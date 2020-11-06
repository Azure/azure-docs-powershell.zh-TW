---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 6905e16667fd2a4378474950d928ef730ed1786e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93612250"
---
# <span data-ttu-id="1f647-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="1f647-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="1f647-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1f647-102">SYNOPSIS</span></span>
<span data-ttu-id="1f647-103">刪除服務實例。</span><span class="sxs-lookup"><span data-stu-id="1f647-103">Deletes a service instance.</span></span>

## <span data-ttu-id="1f647-104">句法</span><span class="sxs-lookup"><span data-stu-id="1f647-104">SYNTAX</span></span>

### <span data-ttu-id="1f647-105">ServiceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1f647-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f647-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f647-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f647-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f647-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f647-108">說明</span><span class="sxs-lookup"><span data-stu-id="1f647-108">DESCRIPTION</span></span>
<span data-ttu-id="1f647-109">刪除服務實例。</span><span class="sxs-lookup"><span data-stu-id="1f647-109">Deletes a service instance.</span></span>

## <span data-ttu-id="1f647-110">示例</span><span class="sxs-lookup"><span data-stu-id="1f647-110">EXAMPLES</span></span>

### <span data-ttu-id="1f647-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1f647-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="1f647-112">刪除提供之資源群組中提供之名稱的現有 HealthcareApis 服務。</span><span class="sxs-lookup"><span data-stu-id="1f647-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="1f647-113">範例2</span><span class="sxs-lookup"><span data-stu-id="1f647-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="1f647-114">刪除擁有所提供 ResourceId 的現有 HealthcareApis 服務。</span><span class="sxs-lookup"><span data-stu-id="1f647-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="1f647-115">範例3</span><span class="sxs-lookup"><span data-stu-id="1f647-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="1f647-116">刪除提供的 HealthcareApis 服務物件。</span><span class="sxs-lookup"><span data-stu-id="1f647-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="1f647-117">參數</span><span class="sxs-lookup"><span data-stu-id="1f647-117">PARAMETERS</span></span>

### <span data-ttu-id="1f647-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f647-118">-AsJob</span></span>
<span data-ttu-id="1f647-119">在背景中執行 Cmdlet 作為作業。</span><span class="sxs-lookup"><span data-stu-id="1f647-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="1f647-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f647-120">-DefaultProfile</span></span>
<span data-ttu-id="1f647-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1f647-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f647-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f647-122">-InputObject</span></span>
<span data-ttu-id="1f647-123">HealthcareApis service 物件</span><span class="sxs-lookup"><span data-stu-id="1f647-123">HealthcareApis service object</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1f647-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="1f647-124">-Name</span></span>
<span data-ttu-id="1f647-125">HealthcareApis 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="1f647-125">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f647-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f647-126">-PassThru</span></span>
<span data-ttu-id="1f647-127">如果有提供，則會在操作成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="1f647-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="1f647-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f647-128">-ResourceGroupName</span></span>
<span data-ttu-id="1f647-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1f647-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f647-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f647-130">-ResourceId</span></span>
<span data-ttu-id="1f647-131">HealthcareApis 服務 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="1f647-131">HealthcareApis Service ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f647-132">-確認</span><span class="sxs-lookup"><span data-stu-id="1f647-132">-Confirm</span></span>
<span data-ttu-id="1f647-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1f647-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f647-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f647-134">-WhatIf</span></span>
<span data-ttu-id="1f647-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1f647-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f647-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1f647-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f647-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f647-137">CommonParameters</span></span>
<span data-ttu-id="1f647-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1f647-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f647-139">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1f647-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f647-140">輸入</span><span class="sxs-lookup"><span data-stu-id="1f647-140">INPUTS</span></span>

### <span data-ttu-id="1f647-141">System.object</span><span class="sxs-lookup"><span data-stu-id="1f647-141">System.String</span></span>

### <span data-ttu-id="1f647-142">PSHealthcareApisService 中的 HealthcareApisService。</span><span class="sxs-lookup"><span data-stu-id="1f647-142">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="1f647-143">輸出</span><span class="sxs-lookup"><span data-stu-id="1f647-143">OUTPUTS</span></span>

### <span data-ttu-id="1f647-144">System.object</span><span class="sxs-lookup"><span data-stu-id="1f647-144">System.Boolean</span></span>

## <span data-ttu-id="1f647-145">筆記</span><span class="sxs-lookup"><span data-stu-id="1f647-145">NOTES</span></span>

## <span data-ttu-id="1f647-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="1f647-146">RELATED LINKS</span></span>
