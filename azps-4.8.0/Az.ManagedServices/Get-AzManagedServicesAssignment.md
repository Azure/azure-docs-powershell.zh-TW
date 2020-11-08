---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/get-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Get-AzManagedServicesAssignment.md
ms.openlocfilehash: 0afa2d4ae6c158accce277ffe3247c5cfd094126
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129473"
---
# <span data-ttu-id="087d1-101">Get-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="087d1-101">Get-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="087d1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="087d1-102">SYNOPSIS</span></span>
<span data-ttu-id="087d1-103">取得註冊作業的清單。</span><span class="sxs-lookup"><span data-stu-id="087d1-103">Gets a list of the registration assignments.</span></span>

## <span data-ttu-id="087d1-104">句法</span><span class="sxs-lookup"><span data-stu-id="087d1-104">SYNTAX</span></span>

### <span data-ttu-id="087d1-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="087d1-105">Default (Default)</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="087d1-106">ById</span><span class="sxs-lookup"><span data-stu-id="087d1-106">ById</span></span>
```
Get-AzManagedServicesAssignment [-Scope <String>] -Id <String> [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="087d1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="087d1-107">ByResourceId</span></span>
```
Get-AzManagedServicesAssignment -ResourceId <String> [-ExpandRegistrationDefinition]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="087d1-108">說明</span><span class="sxs-lookup"><span data-stu-id="087d1-108">DESCRIPTION</span></span>
<span data-ttu-id="087d1-109">取得註冊作業的清單。</span><span class="sxs-lookup"><span data-stu-id="087d1-109">Gets a list of the registration assignments.</span></span>

## <span data-ttu-id="087d1-110">示例</span><span class="sxs-lookup"><span data-stu-id="087d1-110">EXAMPLES</span></span>

### <span data-ttu-id="087d1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="087d1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzManagedServicesAssignment

Name                                 RegistrationDefinitionId
----                                 ------------------------
f2e18995-6c79-4ab7-876e-1b1c8393d12c /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/a156aad7-f3ce-4a46-b240-246242b6bd78
ddd0d277-e120-4de1-8498-52b8f767b699 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/cae481c0-de7c-42a8-86c1-5b170861caf8
```

<span data-ttu-id="087d1-112">取得預設範圍下的所有註冊作業。</span><span class="sxs-lookup"><span data-stu-id="087d1-112">Gets all registration assignments under the default scope.</span></span>

### <span data-ttu-id="087d1-113">範例2</span><span class="sxs-lookup"><span data-stu-id="087d1-113">Example 2</span></span>
```powershell
PS C:\> $assignments = Get-AzManagedServicesAssignment -ExpandRegistrationDefinition
PS C:\> $assignments

Name                                 RegistrationDefinitionId
----                                 ------------------------
f2e18995-6c79-4ab7-876e-1b1c8393d12c /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/a156aad7-f3ce-4a46-b240-246242b6bd78
8b6d4693-efb0-4b58-ac94-625b6a321af3 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/bb2626be-3e11-442f-b0f1-9209508d4f52
ddd0d277-e120-4de1-8498-52b8f767b699 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/cae481c0-de7c-42a8-86c1-5b170861caf8


PS C:\> $assignments[2].Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/cae481c0-de7c-42a8-86c1-5b170861caf8
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : cae481c0-de7c-42a8-86c1-5b170861caf8
```

<span data-ttu-id="087d1-114">取得註冊定義詳細資料的所有註冊作業。</span><span class="sxs-lookup"><span data-stu-id="087d1-114">Gets all registration assignments with the registration definition details.</span></span>

### <span data-ttu-id="087d1-115">範例3</span><span class="sxs-lookup"><span data-stu-id="087d1-115">Example 3</span></span>
```powershell
PS C:\> $assignmnent = Get-AzManagedServicesAssignment -Id ddd0d277-e120-4de1-8498-52b8f767b699
PS C:\> $assignmnent

Name                                 RegistrationDefinitionId
----                                 ------------------------
ddd0d277-e120-4de1-8498-52b8f767b699 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/cae481c0-de7c-42a8-86c1-5b170861caf8

PS C:\> $assignmnent.Properties.RegistrationDefinition

Properties :
Plan       :
Id         :
Type       :
Name       :
```

<span data-ttu-id="087d1-116">在沒有註冊定義詳細資料的情況下，取得註冊作業。</span><span class="sxs-lookup"><span data-stu-id="087d1-116">Gets a registration assignment without the registration definition details.</span></span>

### <span data-ttu-id="087d1-117">範例4</span><span class="sxs-lookup"><span data-stu-id="087d1-117">Example 4</span></span>
```powershell
PS C:\> $assignmnentWithDef = Get-AzManagedServicesAssignment -Id ddd0d277-e120-4de1-8498-52b8f767b699 -ExpandRegistrationDefinition
PS C:\> $assignmnentWithDef

Name                                 RegistrationDefinitionId
----                                 ------------------------
ddd0d277-e120-4de1-8498-52b8f767b699 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/cae481c0-de7c-42a8-86c1-5b170861caf8


PS C:\> $assignmnentWithDef.Properties.RegistrationDefinition


Properties : Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignmentPropertiesRegistrationDefinitionProperties
Plan       :
Id         : /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/cae481c0-de7c-42a8-86c1-5b170861caf8
Type       : Microsoft.ManagedServices/registrationDefinitions
Name       : cae481c0-de7c-42a8-86c1-5b170861caf8
```

<span data-ttu-id="087d1-118">取得含註冊定義詳細資料的註冊作業。</span><span class="sxs-lookup"><span data-stu-id="087d1-118">Gets a registration assignment with registration definition details.</span></span>

### <span data-ttu-id="087d1-119">範例5</span><span class="sxs-lookup"><span data-stu-id="087d1-119">Example 5</span></span>
```powershell
PS C:\> Get-AzManagedServicesAssignment -Scope /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/resourceGroups/newRG

Name                                 RegistrationDefinitionId
----                                 ------------------------
c5deb1ba-8e27-4935-8af5-9242e7dabd24 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/447b1aff-b0fc-4959-989d-d77dc93f3509
aa891268-329a-4637-b3f6-2877ea304f8b /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/46b981a7-63ff-4063-9961-9fce4ddea376
```

<span data-ttu-id="087d1-120">取得所有的註冊作業。</span><span class="sxs-lookup"><span data-stu-id="087d1-120">Gets all the registration assignments.</span></span>

### <span data-ttu-id="087d1-121">範例6</span><span class="sxs-lookup"><span data-stu-id="087d1-121">Example 6</span></span>
```powershell
PS C:\> $assignments = Get-AzManagedServicesAssignment
PS C:\> $assignments[0].Id
/subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationAssignments/f2e18995-6c79-4ab7-876e-1b1c8393d12c
PS C:\> Get-AzManagedServicesAssignment -ResourceId $assignments[0].Id

Name                                 RegistrationDefinitionId
----                                 ------------------------
f2e18995-6c79-4ab7-876e-1b1c8393d12c /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/a156aad7-f3ce-4a46-b240-246242b6bd78
```

<span data-ttu-id="087d1-122">取得已知完全限定資源識別碼的註冊指派。</span><span class="sxs-lookup"><span data-stu-id="087d1-122">Gets the registration assignment given the fully qualified resource id.</span></span>

## <span data-ttu-id="087d1-123">參數</span><span class="sxs-lookup"><span data-stu-id="087d1-123">PARAMETERS</span></span>

### <span data-ttu-id="087d1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="087d1-124">-DefaultProfile</span></span>
<span data-ttu-id="087d1-125">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="087d1-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="087d1-126">-ExpandRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="087d1-126">-ExpandRegistrationDefinition</span></span>
<span data-ttu-id="087d1-127">是否包含註冊定義詳細資料。</span><span class="sxs-lookup"><span data-stu-id="087d1-127">Whether to include registration definition details.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="087d1-128">-識別碼</span><span class="sxs-lookup"><span data-stu-id="087d1-128">-Id</span></span>
<span data-ttu-id="087d1-129">註冊指派識別碼 (例如，b0c052e5-c437-4771-a476-8b1201158a57) 。</span><span class="sxs-lookup"><span data-stu-id="087d1-129">The Registration Assignment identifier (for example, b0c052e5-c437-4771-a476-8b1201158a57).</span></span>
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

### <span data-ttu-id="087d1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="087d1-130">-ResourceId</span></span>
<span data-ttu-id="087d1-131">[註冊作業作業 Id] (例如，/subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationAssignments/b0c052e5-c437-4771-a476-8b1201158a57) </span><span class="sxs-lookup"><span data-stu-id="087d1-131">The Registration Assignment ResourceId (for example, /subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationAssignments/b0c052e5-c437-4771-a476-8b1201158a57)</span></span>
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

### <span data-ttu-id="087d1-132">-範圍</span><span class="sxs-lookup"><span data-stu-id="087d1-132">-Scope</span></span>
<span data-ttu-id="087d1-133">建立註冊作業的範圍。</span><span class="sxs-lookup"><span data-stu-id="087d1-133">The scope where the registration assignment is created.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, ById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="087d1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="087d1-134">CommonParameters</span></span>
<span data-ttu-id="087d1-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="087d1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="087d1-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="087d1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="087d1-137">輸入</span><span class="sxs-lookup"><span data-stu-id="087d1-137">INPUTS</span></span>

### <span data-ttu-id="087d1-138">所有</span><span class="sxs-lookup"><span data-stu-id="087d1-138">None</span></span>

## <span data-ttu-id="087d1-139">輸出</span><span class="sxs-lookup"><span data-stu-id="087d1-139">OUTPUTS</span></span>

### <span data-ttu-id="087d1-140">PSRegistrationAssignment （ManagedServices）的</span><span class="sxs-lookup"><span data-stu-id="087d1-140">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>

## <span data-ttu-id="087d1-141">筆記</span><span class="sxs-lookup"><span data-stu-id="087d1-141">NOTES</span></span>

## <span data-ttu-id="087d1-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="087d1-142">RELATED LINKS</span></span>
