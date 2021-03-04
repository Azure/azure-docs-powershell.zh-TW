---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 5f0398981f6c3a59c9401df4ec89208a5f8196b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905369"
---
# <span data-ttu-id="d949f-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d949f-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="d949f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d949f-102">SYNOPSIS</span></span>
<span data-ttu-id="d949f-103">獲得特定的註冊作業或註冊作業清單。</span><span class="sxs-lookup"><span data-stu-id="d949f-103">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="d949f-104">語法</span><span class="sxs-lookup"><span data-stu-id="d949f-104">SYNTAX</span></span>

### <span data-ttu-id="d949f-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="d949f-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d949f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d949f-106">ByName</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-Name <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d949f-107">描述</span><span class="sxs-lookup"><span data-stu-id="d949f-107">DESCRIPTION</span></span>
<span data-ttu-id="d949f-108">獲得特定的註冊作業或註冊作業清單。</span><span class="sxs-lookup"><span data-stu-id="d949f-108">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="d949f-109">例子</span><span class="sxs-lookup"><span data-stu-id="d949f-109">EXAMPLES</span></span>

### <span data-ttu-id="d949f-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="d949f-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesAssignment

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="d949f-111">在預設範圍內獲得所有註冊指派。</span><span class="sxs-lookup"><span data-stu-id="d949f-111">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="d949f-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="d949f-112">Example 2</span></span>
```
PS C:\> $assignments = Get-AzManagedServicesAssignment -ExpandRegistrationDefinition
PS C:\> $assignments[0].Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : 0c146106-c927-4098-a7ca-30bbcf44a502

PS C:\>
```

<span data-ttu-id="d949f-113">使用註冊定義詳細資料來獲得所有註冊指派。</span><span class="sxs-lookup"><span data-stu-id="d949f-113">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="d949f-114">範例 3</span><span class="sxs-lookup"><span data-stu-id="d949f-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="d949f-115">根據名稱獲得註冊指派，而不提供註冊定義詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d949f-115">Gets a registration assignment by name without registration definition details.</span></span>

### <span data-ttu-id="d949f-116">範例 4</span><span class="sxs-lookup"><span data-stu-id="d949f-116">Example 4</span></span>
```
PS C:\> $assignment = Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80 -ExpandRegistrationDefinition
PS C:\> $assignment.Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationDefinitions/0c146106-c927-4098-a7ca-30bbcf44a502
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : 0c146106-c927-4098-a7ca-30bbcf44a502

PS C:\>
```

<span data-ttu-id="d949f-117">以名稱與註冊定義詳細資料來獲得註冊指派。</span><span class="sxs-lookup"><span data-stu-id="d949f-117">Gets a registration assignment by name with registration definition details.</span></span>

### <span data-ttu-id="d949f-118">範例 5</span><span class="sxs-lookup"><span data-stu-id="d949f-118">Example 5</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="d949f-119">在指定範圍中獲得所有註冊作業。</span><span class="sxs-lookup"><span data-stu-id="d949f-119">Gets all the registration assignments at given scope.</span></span>

## <span data-ttu-id="d949f-120">參數</span><span class="sxs-lookup"><span data-stu-id="d949f-120">PARAMETERS</span></span>

### <span data-ttu-id="d949f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d949f-121">-DefaultProfile</span></span>
<span data-ttu-id="d949f-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d949f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d949f-123">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="d949f-123">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="d949f-124">是否要包含註冊定義詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d949f-124">Whether to include registration definition details.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d949f-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="d949f-125">-Name</span></span>
<span data-ttu-id="d949f-126">註冊作業的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="d949f-126">The unique name of the Registration Assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d949f-127">-範圍</span><span class="sxs-lookup"><span data-stu-id="d949f-127">-Scope</span></span>
<span data-ttu-id="d949f-128">建立註冊作業的範圍。</span><span class="sxs-lookup"><span data-stu-id="d949f-128">The scope where the registration assignment created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d949f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d949f-129">CommonParameters</span></span>
<span data-ttu-id="d949f-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d949f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d949f-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d949f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d949f-132">輸入</span><span class="sxs-lookup"><span data-stu-id="d949f-132">INPUTS</span></span>

### <span data-ttu-id="d949f-133">沒有</span><span class="sxs-lookup"><span data-stu-id="d949f-133">None</span></span>
## <span data-ttu-id="d949f-134">輸出</span><span class="sxs-lookup"><span data-stu-id="d949f-134">OUTPUTS</span></span>

### <span data-ttu-id="d949f-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.models.PSRegistrationAssignment</span><span class="sxs-lookup"><span data-stu-id="d949f-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="d949f-136">筆記</span><span class="sxs-lookup"><span data-stu-id="d949f-136">NOTES</span></span>

## <span data-ttu-id="d949f-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="d949f-137">RELATED LINKS</span></span>
