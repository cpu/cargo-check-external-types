warning: Fields on `custom_lib::test_fields_stripped::SomeStructWithStrippedFields` marked `#[doc(hidden)]` cannot be checked for external types
error: Unapproved external type `external_lib::SimpleTrait` referenced in public API
  --> test-crate-custom-lib-name/src/lib.rs:38:1
   |
38 | pub fn external_in_fn_input(_one: &SomeStruct, _two: impl SimpleTrait) {}
   | ^-----------------------------------------------------------------------^
   |
   = in argument named `_two` of `custom_lib::external_in_fn_input`

error: Unapproved external type `external_lib::SimpleTrait` referenced in public API
  --> test-crate-custom-lib-name/src/lib.rs:38:1
   |
38 | pub fn external_in_fn_input(_one: &SomeStruct, _two: impl SimpleTrait) {}
   | ^-----------------------------------------------------------------------^
   |
   = in trait bound of `custom_lib::external_in_fn_input`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
  --> test-crate-custom-lib-name/src/lib.rs:38:1
   |
38 | pub fn external_in_fn_input(_one: &SomeStruct, _two: impl SimpleTrait) {}
   | ^-----------------------------------------------------------------------^
   |
   = in argument named `_one` of `custom_lib::external_in_fn_input`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
  --> test-crate-custom-lib-name/src/lib.rs:43:1
   |
43 | pub fn external_in_fn_output() -> SomeStruct {
   | ...
45 | }␊
   | ^
   |
   = in return value of `custom_lib::external_in_fn_output`

error: Unapproved external type `external_lib::SimpleTrait` referenced in public API
  --> test-crate-custom-lib-name/src/lib.rs:47:1
   |
47 | pub fn external_opaque_type_in_output() -> impl SimpleTrait {
   | ...
49 | }␊
   | ^
   |
   = in return value of `custom_lib::external_opaque_type_in_output`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
  --> test-crate-custom-lib-name/src/lib.rs:54:1
   |
54 | pub fn external_in_fn_output_generic() -> Option<SomeStruct> {
   | ...
56 | }␊
   | ^
   |
   = in generic arg of `custom_lib::external_in_fn_output_generic`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
  --> test-crate-custom-lib-name/src/lib.rs:62:5
   |
62 |     pub fn something(_one: &SomeStruct) {}
   |     ^------------------------------------^
   |
   = in argument named `_one` of `custom_lib::something`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
  --> test-crate-custom-lib-name/src/lib.rs:67:5
   |
67 |     pub field: SomeStruct,
   |     ^-------------------^
   |
   = in struct field of `custom_lib::StructWithExternalFields::field`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
  --> test-crate-custom-lib-name/src/lib.rs:68:5
   |
68 |     pub optional_field: Option<SomeStruct>,
   |     ^------------------------------------^
   |
   = in generic arg of `custom_lib::StructWithExternalFields::optional_field`

error: Unapproved external type `external_lib::SomeOtherStruct` referenced in public API
  --> test-crate-custom-lib-name/src/lib.rs:72:5
   |
72 |     pub fn new(_field: impl Into<SomeStruct>, _optional_field: Option<SomeOtherStruct>) -> Self {
   | ...
74 |     }␊
   |     ^
   |
   = in generic arg of `custom_lib::StructWithExternalFields::new`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
  --> test-crate-custom-lib-name/src/lib.rs:72:5
   |
72 |     pub fn new(_field: impl Into<SomeStruct>, _optional_field: Option<SomeOtherStruct>) -> Self {
   | ...
74 |     }␊
   |     ^
   |
   = in generic arg of `custom_lib::StructWithExternalFields::new`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
  --> test-crate-custom-lib-name/src/lib.rs:78:5
   |
78 |     fn something(&self, a: SomeStruct) -> LocalStruct;
   |     ^------------------------------------------------^
   |
   = in argument named `a` of `custom_lib::TraitReferencingExternals::something`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
  --> test-crate-custom-lib-name/src/lib.rs:79:5
   |
79 |     fn optional_something(&self, a: Option<SomeStruct>) -> LocalStruct;
   |     ^-----------------------------------------------------------------^
   |
   = in generic arg of `custom_lib::TraitReferencingExternals::optional_something`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
  --> test-crate-custom-lib-name/src/lib.rs:80:5
   |
80 |     fn otherthing(&self) -> SomeStruct;
   |     ^---------------------------------^
   |
   = in return value of `custom_lib::TraitReferencingExternals::otherthing`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
  --> test-crate-custom-lib-name/src/lib.rs:81:5
   |
81 |     fn optional_otherthing(&self) -> Option<SomeStruct>;
   |     ^--------------------------------------------------^
   |
   = in generic arg of `custom_lib::TraitReferencingExternals::optional_otherthing`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
  --> test-crate-custom-lib-name/src/lib.rs:84:1
   |
84 | pub enum EnumWithExternals<T = SomeStruct> {
   | ...
98 | }␊
   | ^
   |
   = in generic default binding of `custom_lib::EnumWithExternals`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
  --> test-crate-custom-lib-name/src/lib.rs:89:15
   |
89 |     TupleEnum(SomeStruct, Box<dyn SimpleTrait>),
   |               ^--------^
   |
   = in struct field of `custom_lib::EnumWithExternals::TupleEnum::0`

error: Unapproved external type `external_lib::SimpleTrait` referenced in public API
  --> test-crate-custom-lib-name/src/lib.rs:89:27
   |
89 |     TupleEnum(SomeStruct, Box<dyn SimpleTrait>),
   |                           ^------------------^
   |
   = in dyn trait of `custom_lib::EnumWithExternals::TupleEnum::1`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
  --> test-crate-custom-lib-name/src/lib.rs:91:9
   |
91 |         some_struct: SomeStruct,
   |         ^---------------------^
   |
   = in struct field of `custom_lib::EnumWithExternals::StructEnum::some_struct`

error: Unapproved external type `external_lib::SimpleTrait` referenced in public API
  --> test-crate-custom-lib-name/src/lib.rs:92:9
   |
92 |         simple_trait: Box<dyn SimpleTrait>,
   |         ^--------------------------------^
   |
   = in dyn trait of `custom_lib::EnumWithExternals::StructEnum::simple_trait`

error: Unapproved external type `external_lib::SimpleTrait` referenced in public API
   --> test-crate-custom-lib-name/src/lib.rs:104:5
    |
104 |     pub fn another_thing<S: SimpleTrait>(_s: S) -> Self {
    | ...
106 |     }␊
    |     ^
    |
    = in trait bound of `custom_lib::EnumWithExternals::another_thing`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
   --> test-crate-custom-lib-name/src/lib.rs:109:1
    |
109 | pub static SOME_STRUCT: SomeStruct = SomeStruct;
    | ^----------------------------------------------^
    |
    = in static value `custom_lib::SOME_STRUCT`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
   --> test-crate-custom-lib-name/src/lib.rs:110:1
    |
110 | pub const SOME_CONST: SomeStruct = SomeStruct;
    | ^--------------------------------------------^
    |
    = in constant `custom_lib::SOME_CONST`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
   --> test-crate-custom-lib-name/src/lib.rs:115:5
    |
115 |     pub static OPTIONAL_STRUCT: Option<SomeStruct> = None;
    |     ^----------------------------------------------------^
    |
    = in generic arg of `custom_lib::some_pub_mod::OPTIONAL_STRUCT`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
   --> test-crate-custom-lib-name/src/lib.rs:116:5
    |
116 |     pub const OPTIONAL_CONST: Option<SomeStruct> = None;
    |     ^--------------------------------------------------^
    |
    = in generic arg of `custom_lib::some_pub_mod::OPTIONAL_CONST`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
   --> test-crate-custom-lib-name/src/lib.rs:120:1
    |
120 | pub type ExternalReferencingTypeAlias = SomeStruct;
    | ^-------------------------------------------------^
    |
    = in type alias of `custom_lib::ExternalReferencingTypeAlias`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
   --> test-crate-custom-lib-name/src/lib.rs:121:1
    |
121 | pub type OptionalExternalReferencingTypeAlias = Option<SomeStruct>;
    | ^-----------------------------------------------------------------^
    |
    = in generic arg of `custom_lib::OptionalExternalReferencingTypeAlias`

error: Unapproved external type `external_lib::SimpleTrait` referenced in public API
   --> test-crate-custom-lib-name/src/lib.rs:122:1
    |
122 | pub type DynExternalReferencingTypeAlias = Box<dyn SimpleTrait>;
    | ^--------------------------------------------------------------^
    |
    = in dyn trait of `custom_lib::DynExternalReferencingTypeAlias`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
   --> test-crate-custom-lib-name/src/lib.rs:123:1
    |
123 | pub type ExternalReferencingRawPtr = *const SomeStruct;
    | ^-----------------------------------------------------^
    |
    = in type alias of `custom_lib::ExternalReferencingRawPtr`

error: Unapproved external type `external_lib::AssociatedGenericTrait` referenced in public API
   --> test-crate-custom-lib-name/src/lib.rs:125:1
    |
125 | pub fn fn_with_external_trait_bounds<I, O, E, T>(_thing: T)
    | ...
132 | }␊
    | ^
    |
    = in trait bound of `custom_lib::fn_with_external_trait_bounds`

error: Unapproved external type `external_lib::SomeOtherStruct` referenced in public API
   --> test-crate-custom-lib-name/src/lib.rs:125:1
    |
125 | pub fn fn_with_external_trait_bounds<I, O, E, T>(_thing: T)
    | ...
132 | }␊
    | ^
    |
    = in generic arg of `custom_lib::fn_with_external_trait_bounds`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
   --> test-crate-custom-lib-name/src/lib.rs:125:1
    |
125 | pub fn fn_with_external_trait_bounds<I, O, E, T>(_thing: T)
    | ...
132 | }␊
    | ^
    |
    = in generic arg of `custom_lib::fn_with_external_trait_bounds`

error: Unapproved external type `external_lib::SimpleTrait` referenced in public API
   --> test-crate-custom-lib-name/src/lib.rs:135:5
    |
135 |     type Thing: SimpleTrait;
    |     ^----------------------^
    |
    = in trait bound of `custom_lib::SomeTraitWithExternalDefaultTypes::Thing`

error: Unapproved external type `external_lib::AssociatedGenericTrait` referenced in public API
   --> test-crate-custom-lib-name/src/lib.rs:136:5
    |
136 |     type OtherThing: AssociatedGenericTrait<
    | ...
140 |     >;␊
    |     ^^
    |
    = in trait bound of `custom_lib::SomeTraitWithExternalDefaultTypes::OtherThing`

error: Unapproved external type `external_lib::SomeOtherStruct` referenced in public API
   --> test-crate-custom-lib-name/src/lib.rs:136:5
    |
136 |     type OtherThing: AssociatedGenericTrait<
    | ...
140 |     >;␊
    |     ^^
    |
    = in generic default binding of `custom_lib::SomeTraitWithExternalDefaultTypes::OtherThing`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
   --> test-crate-custom-lib-name/src/lib.rs:136:5
    |
136 |     type OtherThing: AssociatedGenericTrait<
    | ...
140 |     >;␊
    |     ^^
    |
    = in generic default binding of `custom_lib::SomeTraitWithExternalDefaultTypes::OtherThing`

error: Unapproved external type `external_lib::SimpleTrait` referenced in public API
   --> test-crate-custom-lib-name/src/lib.rs:146:5
    |
146 |     type MyGAT<T>
    | ...
148 |         T: SimpleTrait;␊
    |     ^-----------------^
    |
    = in trait bound of `custom_lib::SomeTraitWithGenericAssociatedType::MyGAT`

error: Unapproved external type `external_lib::SimpleTrait` referenced in public API
   --> test-crate-custom-lib-name/src/lib.rs:150:5
    |
150 |     fn some_fn<T: SimpleTrait>(&self, thing: Self::MyGAT<T>);
    |     ^-------------------------------------------------------^
    |
    = in trait bound of `custom_lib::SomeTraitWithGenericAssociatedType::some_fn`

error: Unapproved external type `external_lib::SimpleNewType` referenced in public API
   --> test-crate-custom-lib-name/src/lib.rs:158:5
    |
158 |     pub const OTHER_CONST: SimpleNewType = SimpleNewType(5);
    |     ^------------------------------------------------------^
    |
    = in struct field of `custom_lib::AssocConstStruct::OTHER_CONST`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
  --> test-crate-custom-lib-name/src/test_assoc_type.rs:12:5
   |
12 |     type Error = SomeStruct;
   |     ^----------------------^
   |
   = in associated type `custom_lib::test_assoc_type::PublicStructImplsTraitWithExtAssocType::Error`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
  --> test-crate-custom-lib-name/src/test_assoc_type.rs:55:5
   |
55 |     type Something = Result<(), SomeStruct>;
   |     ^--------------------------------------^
   |
   = in generic arg of `custom_lib::test_assoc_type::PublicStructImplsPublicTraitWithAssocType::Something`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
 --> test-crate-custom-lib-name/src/test_structs.rs:8:40
  |
8 | pub struct TupleStructWithExternalType(pub external_lib::SomeStruct);
  |                                        ^--------------------------^
  |
  = in struct field of `custom_lib::test_structs::TupleStructWithExternalType::0`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
  --> test-crate-custom-lib-name/src/test_structs.rs:14:5
   |
14 |     pub external: external_lib::SomeStruct,
   |     ^------------------------------------^
   |
   = in struct field of `custom_lib::test_structs::PlainStructWithExternalType::external`

error: Unapproved external type `external_lib::SimpleGenericTrait` referenced in public API
  --> test-crate-custom-lib-name/src/test_structs.rs:27:1
   |
27 | impl external_lib::SimpleGenericTrait<external_lib::SomeStruct> for ImplsGenericTrait {
   | ...
31 | }␊
   | ^
   |
   = in implemented trait of `custom_lib::test_structs::ImplsGenericTrait`

error: Unapproved external type `external_lib::SomeStruct` referenced in public API
  --> test-crate-custom-lib-name/src/test_structs.rs:27:1
   |
27 | impl external_lib::SimpleGenericTrait<external_lib::SomeStruct> for ImplsGenericTrait {
   | ...
31 | }␊
   | ^
   |
   = in generic arg of `custom_lib::test_structs::ImplsGenericTrait`

error: Unapproved external type `external_lib::ReprCType` referenced in public API
  --> test-crate-custom-lib-name/src/test_union.rs:10:5
   |
10 |     pub repr_c: ReprCType,
   |     ^-------------------^
   |
   = in struct field of `custom_lib::test_union::SimpleUnion::repr_c`

error: Unapproved external type `external_lib::ReprCType` referenced in public API
  --> test-crate-custom-lib-name/src/test_union.rs:15:5
   |
15 |     pub fn repr_c(&self) -> &ReprCType {
   | ...
17 |     }␊
   |     ^
   |
   = in return value of `custom_lib::test_union::SimpleUnion::repr_c`

error: Unapproved external type `external_lib::SimpleTrait` referenced in public API
  --> test-crate-custom-lib-name/src/test_union.rs:21:1
   |
21 | pub union GenericUnion<T: Copy + SimpleTrait> {
   | ...
24 | }␊
   | ^
   |
   = in trait bound of `custom_lib::test_union::GenericUnion`

48 errors, 1 warnings emitted
