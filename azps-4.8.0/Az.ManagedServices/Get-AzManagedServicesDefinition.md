---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesDefinition.md
ms.openlocfilehash: a4a365cdaee79a39b87331c42c832e40f7cbd657
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129475"
---
# <span data-ttu-id="4e4e5-101">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="4e4e5-101">Get-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="4e4e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e4e5-102">SYNOPSIS</span></span>
<span data-ttu-id="4e4e5-103">取得註冊定義的清單。</span><span class="sxs-lookup"><span data-stu-id="4e4e5-103">Gets a list of the registration definitions.</span></span>

## <span data-ttu-id="4e4e5-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e4e5-104">SYNTAX</span></span>

### <span data-ttu-id="4e4e5-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="4e4e5-105">Default (Default)</span></span>
```
Get-AzManagedServicesDefinition [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e4e5-106">ById</span><span class="sxs-lookup"><span data-stu-id="4e4e5-106">ById</span></span>
```
Get-AzManagedServicesDefinition -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e4e5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4e4e5-107">ByResourceId</span></span>
```
Get-AzManagedServicesDefinition -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e4e5-108">說明</span><span class="sxs-lookup"><span data-stu-id="4e4e5-108">DESCRIPTION</span></span>
<span data-ttu-id="4e4e5-109">取得註冊定義的清單。</span><span class="sxs-lookup"><span data-stu-id="4e4e5-109">Gets a list of the registration definitions.</span></span>

## <span data-ttu-id="4e4e5-110">示例</span><span class="sxs-lookup"><span data-stu-id="4e4e5-110">EXAMPLES</span></span>

### <span data-ttu-id="4e4e5-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4e4e5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzManagedServicesDefinition

Name                                 ManagedByTenantId                    PrincipalId                                                                  RoleDefinitionId
----                                 -----------------                    -----------                                                                  ----------------
fff287a4-1714-4a17-bc40-a17ca8e69e3f bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671                                         acdd72a7-3385-48ef-bd42-f606fba81ae7
ee7e40e8-bc3f-4624-b0ca-d5364635b141 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671                                         acdd72a7-3385-48ef-bd42-f606fba81ae7
e2ddcd3c-d50f-4d51-afd9-f9132fcae4e7 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671                                         acdd72a7-3385-48ef-bd42-f606fba81ae7
d3301f65-7087-438c-a6bc-4b7ead094889 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671                                         acdd72a7-3385-48ef-bd42-f606fba81ae7
cae481c0-de7c-42a8-86c1-5b170861caf8 bab3375b-6197-4a15-a44b-16c41faa91d7 {d6f6c88a-5b7a-455e-ba40-ce146d4d3671, d6f6c88a-5b7a-455e-ba40-ce146d4d3671} {acdd72a7-3385-48ef-bd42-f606fba81ae7, b24988ac-6180-42a0-ab88-20f7382dd24c}
bb2626be-3e11-442f-b0f1-9209508d4f52 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671                                         acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="4e4e5-112">取得所有的註冊定義。</span><span class="sxs-lookup"><span data-stu-id="4e4e5-112">Gets all registration definitions.</span></span>

### <span data-ttu-id="4e4e5-113">範例2</span><span class="sxs-lookup"><span data-stu-id="4e4e5-113">Example 2</span></span>
```powershell
PS C:\> Get-AzManagedServicesDefinition -Id fff287a4-1714-4a17-bc40-a17ca8e69e3f

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
fff287a4-1714-4a17-bc40-a17ca8e69e3f bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="4e4e5-114">取得已知識別碼的註冊定義。</span><span class="sxs-lookup"><span data-stu-id="4e4e5-114">Gets the registration definition given its id.</span></span>

### <span data-ttu-id="4e4e5-115">範例3</span><span class="sxs-lookup"><span data-stu-id="4e4e5-115">Example 3</span></span>
```powershell
PS C:\> $definitions = Get-AzManagedServicesDefinition
PS C:\> $definitions[0].Id
/subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/fff287a4-1714-4a17-bc40-a17ca8e69e3f
PS C:\> Get-AzManagedServicesDefinition -ResourceId $definitions[0].Id

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
fff287a4-1714-4a17-bc40-a17ca8e69e3f bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="4e4e5-116">取得已知完全限定資源識別碼的註冊定義。</span><span class="sxs-lookup"><span data-stu-id="4e4e5-116">Gets the registration definition given the fully qualified resource id.</span></span>

## <span data-ttu-id="4e4e5-117">參數</span><span class="sxs-lookup"><span data-stu-id="4e4e5-117">PARAMETERS</span></span>

### <span data-ttu-id="4e4e5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e4e5-118">-DefaultProfile</span></span>
<span data-ttu-id="4e4e5-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e4e5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e4e5-120">-識別碼</span><span class="sxs-lookup"><span data-stu-id="4e4e5-120">-Id</span></span>
<span data-ttu-id="4e4e5-121">註冊定義識別碼 (例如，b0c052e5-c437-4771-a476-8b1201158a57) 。</span><span class="sxs-lookup"><span data-stu-id="4e4e5-121">The registration definition identifier (for example, b0c052e5-c437-4771-a476-8b1201158a57).</span></span>
```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e4e5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e4e5-122">-ResourceId</span></span>
<span data-ttu-id="4e4e5-123">註冊定義的完全限定資源識別碼 (例如，/subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationDefinitions/b0c052e5-c437-4771-a476-8b1201158a57) </span><span class="sxs-lookup"><span data-stu-id="4e4e5-123">The fully qualified resource id of the registration definition (for example, /subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationDefinitions/b0c052e5-c437-4771-a476-8b1201158a57)</span></span>
```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e4e5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e4e5-124">CommonParameters</span></span>
<span data-ttu-id="4e4e5-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e4e5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e4e5-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4e4e5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e4e5-127">輸入</span><span class="sxs-lookup"><span data-stu-id="4e4e5-127">INPUTS</span></span>

### <span data-ttu-id="4e4e5-128">所有</span><span class="sxs-lookup"><span data-stu-id="4e4e5-128">None</span></span>

## <span data-ttu-id="4e4e5-129">輸出</span><span class="sxs-lookup"><span data-stu-id="4e4e5-129">OUTPUTS</span></span>

### <span data-ttu-id="4e4e5-130">PSRegistrationDefinition （ManagedServices）的</span><span class="sxs-lookup"><span data-stu-id="4e4e5-130">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="4e4e5-131">筆記</span><span class="sxs-lookup"><span data-stu-id="4e4e5-131">NOTES</span></span>

## <span data-ttu-id="4e4e5-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e4e5-132">RELATED LINKS</span></span>
