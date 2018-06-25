load("//grammars:pegjs.bzl", "pegjs_grammar")

pegjs_grammar(
    name = "toplevel",
    varname = "toplevelGrammar",
    srcs = ["toplevel.pegjs"],
    visibility = ["//visibility:public"],
    startrules = ["Source", "Decl", "ClassBody", "ClassDecl", "VarDecl", "Statement", "Factor", "QualifiedName", "Expression"],
)

load("@org_pubref_rules_node//node:rules.bzl", "mocha_test")

mocha_test(
    name = "toplevel_test",
    main = "toplevel_test.js",
    deps = [
      "@yarn_modules//:_all_",
      ":toplevel",
    ],
)