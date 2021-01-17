---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 8aae61e163baf95cbed62ea239c7d1a6190aed1f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436481"
---
# <span data-ttu-id="293c6-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="293c6-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="293c6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="293c6-102">SYNOPSIS</span></span>
<span data-ttu-id="293c6-103">取得特定的註冊指派或註冊作業的清單。</span><span class="sxs-lookup"><span data-stu-id="293c6-103">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="293c6-104">句法</span><span class="sxs-lookup"><span data-stu-id="293c6-104">SYNTAX</span></span>

### <span data-ttu-id="293c6-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="293c6-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="293c6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="293c6-106">ByName</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-Name <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="293c6-107">說明</span><span class="sxs-lookup"><span data-stu-id="293c6-107">DESCRIPTION</span></span>
<span data-ttu-id="293c6-108">取得特定的註冊指派或註冊作業的清單。</span><span class="sxs-lookup"><span data-stu-id="293c6-108">Gets a specific registration assignment or a list of the registration assignments.</span></span>

## <span data-ttu-id="293c6-109">示例</span><span class="sxs-lookup"><span data-stu-id="293c6-109">EXAMPLES</span></span>

### <span data-ttu-id="293c6-110">範例1</span><span class="sxs-lookup"><span data-stu-id="293c6-110">Example 1</span></span>
```
PS C:\> Get-AzManagedServicesAssignment

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="293c6-111">取得預設範圍下的所有註冊作業。</span><span class="sxs-lookup"><span data-stu-id="293c6-111">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="293c6-112">範例2</span><span class="sxs-lookup"><span data-stu-id="293c6-112">Example 2</span></span>
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

<span data-ttu-id="293c6-113">取得註冊定義詳細資料的所有註冊作業。</span><span class="sxs-lookup"><span data-stu-id="293c6-113">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="293c6-114">範例3</span><span class="sxs-lookup"><span data-stu-id="293c6-114">Example 3</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Name 0413e647-6915-45e3-944d-79a587e57f80

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="293c6-115">透過名稱取得登記指派（不含註冊定義詳細資料）。</span><span class="sxs-lookup"><span data-stu-id="293c6-115">Gets a registration assignment by name without registration definition details.</span></span>

### <span data-ttu-id="293c6-116">範例4</span><span class="sxs-lookup"><span data-stu-id="293c6-116">Example 4</span></span>
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

<span data-ttu-id="293c6-117">透過名稱取得註冊定義詳細資料的註冊作業。</span><span class="sxs-lookup"><span data-stu-id="293c6-117">Gets a registration assignment by name with registration definition details.</span></span>

### <span data-ttu-id="293c6-118">範例5</span><span class="sxs-lookup"><span data-stu-id="293c6-118">Example 5</span></span>
```
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8

Name                                 Id                                                                                                                                                   ProvisioningState
----                                 --                                                                                                                                                   -----------------
0413e647-6915-45e3-944d-79a587e57f80 /subscriptions/24ab6047-da91-48c0-66e5-20a8c6daefc8/providers/Microsoft.ManagedServices/registrationAssignments/0413e647-6915-45e3-944d-79a587e57f80 Succeeded

PS C:\>
```

<span data-ttu-id="293c6-119">取得指定範圍內的所有註冊作業。</span><span class="sxs-lookup"><span data-stu-id="293c6-119">Gets all the registration assignments at given scope.</span></span>

## <span data-ttu-id="293c6-120">參數</span><span class="sxs-lookup"><span data-stu-id="293c6-120">PARAMETERS</span></span>

### <span data-ttu-id="293c6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="293c6-121">-DefaultProfile</span></span>
<span data-ttu-id="293c6-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="293c6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="293c6-123">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="293c6-123">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="293c6-124">是否包含註冊定義詳細資料。</span><span class="sxs-lookup"><span data-stu-id="293c6-124">Whether to include registration definition details.</span></span>

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

### <span data-ttu-id="293c6-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="293c6-125">-Name</span></span>
<span data-ttu-id="293c6-126">註冊作業的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="293c6-126">The unique name of the Registration Assignment.</span></span>

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

### <span data-ttu-id="293c6-127">-範圍</span><span class="sxs-lookup"><span data-stu-id="293c6-127">-Scope</span></span>
<span data-ttu-id="293c6-128">已建立註冊作業的範圍。</span><span class="sxs-lookup"><span data-stu-id="293c6-128">The scope where the registration assignment created.</span></span>

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

### <span data-ttu-id="293c6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="293c6-129">CommonParameters</span></span>
<span data-ttu-id="293c6-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="293c6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="293c6-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="293c6-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="293c6-132">輸入</span><span class="sxs-lookup"><span data-stu-id="293c6-132">INPUTS</span></span>

### <span data-ttu-id="293c6-133">所有</span><span class="sxs-lookup"><span data-stu-id="293c6-133">None</span></span>
## <span data-ttu-id="293c6-134">輸出</span><span class="sxs-lookup"><span data-stu-id="293c6-134">OUTPUTS</span></span>

### <span data-ttu-id="293c6-135">PSRegistrationAssignment （ManagedServices）的</span><span class="sxs-lookup"><span data-stu-id="293c6-135">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>
## <span data-ttu-id="293c6-136">筆記</span><span class="sxs-lookup"><span data-stu-id="293c6-136">NOTES</span></span>

## <span data-ttu-id="293c6-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="293c6-137">RELATED LINKS</span></span>
