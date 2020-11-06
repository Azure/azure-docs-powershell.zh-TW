---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesAssignment.md
ms.openlocfilehash: 47a76f15700a4697dc7256d73c30ef96eb21523c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611875"
---
# <span data-ttu-id="eb0a4-101">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="eb0a4-101">Remove-AzManagedServicesAssignment</span></span>

## <span data-ttu-id="eb0a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb0a4-102">SYNOPSIS</span></span>
<span data-ttu-id="eb0a4-103">刪除註冊作業。</span><span class="sxs-lookup"><span data-stu-id="eb0a4-103">Deletes a registration assignment.</span></span>

## <span data-ttu-id="eb0a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb0a4-104">SYNTAX</span></span>

### <span data-ttu-id="eb0a4-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="eb0a4-105">Default (Default)</span></span>
```
Remove-AzManagedServicesAssignment [[-Scope] <String>] -Id <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb0a4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="eb0a4-106">ByResourceId</span></span>
```
Remove-AzManagedServicesAssignment -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb0a4-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="eb0a4-107">ByInputObject</span></span>
```
Remove-AzManagedServicesAssignment -InputObject <PSRegistrationAssignment> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb0a4-108">說明</span><span class="sxs-lookup"><span data-stu-id="eb0a4-108">DESCRIPTION</span></span>
<span data-ttu-id="eb0a4-109">刪除註冊作業。</span><span class="sxs-lookup"><span data-stu-id="eb0a4-109">Deletes a registration assignment.</span></span>

## <span data-ttu-id="eb0a4-110">示例</span><span class="sxs-lookup"><span data-stu-id="eb0a4-110">EXAMPLES</span></span>

### <span data-ttu-id="eb0a4-111">範例1</span><span class="sxs-lookup"><span data-stu-id="eb0a4-111">Example 1</span></span>
```powershell
PS C:\Remove-AzManagedServicesAssignment -Id b037e73c-815e-4472-868f-59e51b49b949

Name                                 RegistrationDefinitionId
----                                 ------------------------
b037e73c-815e-4472-868f-59e51b49b949 /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/be2f72e6-93e0-4d3f-ac50-9a756ed4ffa7
```

<span data-ttu-id="eb0a4-112">刪除預設範圍下的註冊作業。</span><span class="sxs-lookup"><span data-stu-id="eb0a4-112">Deletes the registration assignment under the default scope.</span></span>

### <span data-ttu-id="eb0a4-113">範例2</span><span class="sxs-lookup"><span data-stu-id="eb0a4-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzManagedServicesAssignment -ResourceId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationAssignments/88ba878b-9a3c-40c3-80da-015cbe488a2f

Name                                 RegistrationDefinitionId
----                                 ------------------------
88ba878b-9a3c-40c3-80da-015cbe488a2f /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/40be0299-6573-4391-be2f-b41dd4aaf4f9
```

<span data-ttu-id="eb0a4-114">在已知完全限定的資源識別碼的情況下，刪除註冊指派。</span><span class="sxs-lookup"><span data-stu-id="eb0a4-114">Deletes the registration assignment given the fully qualified resource id.</span></span>

### <span data-ttu-id="eb0a4-115">範例3</span><span class="sxs-lookup"><span data-stu-id="eb0a4-115">Example 3</span></span>
```powershell
PS C:\> $assignment = New-AzManagedServicesAssignment -RegistrationDefinitionId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/33974646-9bce-461d-89eb-331f20fca33c
PS C:\> Remove-AzManagedServicesAssignment -InputObject $assignment
```

<span data-ttu-id="eb0a4-116">使用提供的輸入物件刪除註冊作業。</span><span class="sxs-lookup"><span data-stu-id="eb0a4-116">Deletes the registration assignment using the input object provided.</span></span>

## <span data-ttu-id="eb0a4-117">參數</span><span class="sxs-lookup"><span data-stu-id="eb0a4-117">PARAMETERS</span></span>

### <span data-ttu-id="eb0a4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eb0a4-118">-AsJob</span></span>
<span data-ttu-id="eb0a4-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="eb0a4-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="eb0a4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb0a4-120">-DefaultProfile</span></span>
<span data-ttu-id="eb0a4-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eb0a4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb0a4-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="eb0a4-122">-Id</span></span>
<span data-ttu-id="eb0a4-123">註冊指派 GUID (例如，b0c052e5-c437-4771-a476-8b1201158a57) </span><span class="sxs-lookup"><span data-stu-id="eb0a4-123">The registration assignment GUID (for example, b0c052e5-c437-4771-a476-8b1201158a57)</span></span>
```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb0a4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eb0a4-124">-InputObject</span></span>
<span data-ttu-id="eb0a4-125">[註冊指派] 物件。</span><span class="sxs-lookup"><span data-stu-id="eb0a4-125">The registration assignment object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb0a4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eb0a4-126">-ResourceId</span></span>
<span data-ttu-id="eb0a4-127">註冊作業的完全限定資源識別碼 (例如，/subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationAssignments/b0c052e5-c437-4771-a476-8b1201158a57) ]。</span><span class="sxs-lookup"><span data-stu-id="eb0a4-127">The fully qualified resource id of the registration assignment (for example, /subscriptions/bb6d49b2-603d-489f-b6ca-ca4dc497c749/providers/Microsoft.ManagedServices/registrationAssignments/b0c052e5-c437-4771-a476-8b1201158a57).</span></span>

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

### <span data-ttu-id="eb0a4-128">-範圍</span><span class="sxs-lookup"><span data-stu-id="eb0a4-128">-Scope</span></span>
<span data-ttu-id="eb0a4-129">應建立註冊作業的範圍。</span><span class="sxs-lookup"><span data-stu-id="eb0a4-129">The scope where the registration assignment should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb0a4-130">-確認</span><span class="sxs-lookup"><span data-stu-id="eb0a4-130">-Confirm</span></span>
<span data-ttu-id="eb0a4-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eb0a4-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb0a4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb0a4-132">-WhatIf</span></span>
<span data-ttu-id="eb0a4-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="eb0a4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb0a4-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="eb0a4-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb0a4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb0a4-135">CommonParameters</span></span>
<span data-ttu-id="eb0a4-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb0a4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb0a4-137">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="eb0a4-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb0a4-138">輸入</span><span class="sxs-lookup"><span data-stu-id="eb0a4-138">INPUTS</span></span>

### <span data-ttu-id="eb0a4-139">System.object</span><span class="sxs-lookup"><span data-stu-id="eb0a4-139">System.String</span></span>

### <span data-ttu-id="eb0a4-140">PSRegistrationAssignment （ManagedServices）的</span><span class="sxs-lookup"><span data-stu-id="eb0a4-140">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationAssignment</span></span>

## <span data-ttu-id="eb0a4-141">輸出</span><span class="sxs-lookup"><span data-stu-id="eb0a4-141">OUTPUTS</span></span>

### <span data-ttu-id="eb0a4-142">PSRegistrationDefinition （ManagedServices）的</span><span class="sxs-lookup"><span data-stu-id="eb0a4-142">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="eb0a4-143">筆記</span><span class="sxs-lookup"><span data-stu-id="eb0a4-143">NOTES</span></span>

## <span data-ttu-id="eb0a4-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb0a4-144">RELATED LINKS</span></span>
