---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 12db158089473c5f0cfb01e24b762ecf192f8991
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93796929"
---
# <span data-ttu-id="3fde5-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="3fde5-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="3fde5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3fde5-102">SYNOPSIS</span></span>
<span data-ttu-id="3fde5-103">刪除服務實例。</span><span class="sxs-lookup"><span data-stu-id="3fde5-103">Deletes a service instance.</span></span>

## <span data-ttu-id="3fde5-104">句法</span><span class="sxs-lookup"><span data-stu-id="3fde5-104">SYNTAX</span></span>

### <span data-ttu-id="3fde5-105">ServiceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3fde5-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fde5-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fde5-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fde5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3fde5-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fde5-108">說明</span><span class="sxs-lookup"><span data-stu-id="3fde5-108">DESCRIPTION</span></span>
<span data-ttu-id="3fde5-109">刪除服務實例。</span><span class="sxs-lookup"><span data-stu-id="3fde5-109">Deletes a service instance.</span></span>

## <span data-ttu-id="3fde5-110">示例</span><span class="sxs-lookup"><span data-stu-id="3fde5-110">EXAMPLES</span></span>

### <span data-ttu-id="3fde5-111">範例1</span><span class="sxs-lookup"><span data-stu-id="3fde5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="3fde5-112">刪除提供之資源群組中提供之名稱的現有 HealthcareApis 服務。</span><span class="sxs-lookup"><span data-stu-id="3fde5-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="3fde5-113">範例2</span><span class="sxs-lookup"><span data-stu-id="3fde5-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="3fde5-114">刪除擁有所提供 ResourceId 的現有 HealthcareApis 服務。</span><span class="sxs-lookup"><span data-stu-id="3fde5-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="3fde5-115">範例3</span><span class="sxs-lookup"><span data-stu-id="3fde5-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="3fde5-116">刪除提供的 HealthcareApis 服務物件。</span><span class="sxs-lookup"><span data-stu-id="3fde5-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="3fde5-117">參數</span><span class="sxs-lookup"><span data-stu-id="3fde5-117">PARAMETERS</span></span>

### <span data-ttu-id="3fde5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3fde5-118">-AsJob</span></span>
<span data-ttu-id="3fde5-119">在背景中執行 Cmdlet 作為作業。</span><span class="sxs-lookup"><span data-stu-id="3fde5-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="3fde5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fde5-120">-DefaultProfile</span></span>
<span data-ttu-id="3fde5-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3fde5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fde5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fde5-122">-InputObject</span></span>
<span data-ttu-id="3fde5-123">HealthcareApis service 物件</span><span class="sxs-lookup"><span data-stu-id="3fde5-123">HealthcareApis service object</span></span>

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

### <span data-ttu-id="3fde5-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="3fde5-124">-Name</span></span>
<span data-ttu-id="3fde5-125">HealthcareApis 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="3fde5-125">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="3fde5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fde5-126">-PassThru</span></span>
<span data-ttu-id="3fde5-127">如果有提供，則會在操作成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="3fde5-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="3fde5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fde5-128">-ResourceGroupName</span></span>
<span data-ttu-id="3fde5-129">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="3fde5-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="3fde5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fde5-130">-ResourceId</span></span>
<span data-ttu-id="3fde5-131">HealthcareApis 服務 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="3fde5-131">HealthcareApis Service ResourceId.</span></span>

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

### <span data-ttu-id="3fde5-132">-確認</span><span class="sxs-lookup"><span data-stu-id="3fde5-132">-Confirm</span></span>
<span data-ttu-id="3fde5-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3fde5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fde5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fde5-134">-WhatIf</span></span>
<span data-ttu-id="3fde5-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3fde5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fde5-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3fde5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fde5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fde5-137">CommonParameters</span></span>
<span data-ttu-id="3fde5-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3fde5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fde5-139">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3fde5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fde5-140">輸入</span><span class="sxs-lookup"><span data-stu-id="3fde5-140">INPUTS</span></span>

### <span data-ttu-id="3fde5-141">System.object</span><span class="sxs-lookup"><span data-stu-id="3fde5-141">System.String</span></span>

### <span data-ttu-id="3fde5-142">PSHealthcareApisService 中的 HealthcareApisService。</span><span class="sxs-lookup"><span data-stu-id="3fde5-142">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="3fde5-143">輸出</span><span class="sxs-lookup"><span data-stu-id="3fde5-143">OUTPUTS</span></span>

### <span data-ttu-id="3fde5-144">System.object</span><span class="sxs-lookup"><span data-stu-id="3fde5-144">System.Boolean</span></span>

## <span data-ttu-id="3fde5-145">筆記</span><span class="sxs-lookup"><span data-stu-id="3fde5-145">NOTES</span></span>

## <span data-ttu-id="3fde5-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="3fde5-146">RELATED LINKS</span></span>