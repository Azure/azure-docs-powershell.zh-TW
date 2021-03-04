---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/powershell/module/az.healthcareapis/remove-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Remove-AzHealthcareApisService.md
ms.openlocfilehash: 448b400d4a01924d7ef2ce64acc0f7edf827b827
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917214"
---
# <span data-ttu-id="05653-101">Remove-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="05653-101">Remove-AzHealthcareApisService</span></span>

## <span data-ttu-id="05653-102">簡介</span><span class="sxs-lookup"><span data-stu-id="05653-102">SYNOPSIS</span></span>
<span data-ttu-id="05653-103">刪除服務實例。</span><span class="sxs-lookup"><span data-stu-id="05653-103">Deletes a service instance.</span></span>

## <span data-ttu-id="05653-104">語法</span><span class="sxs-lookup"><span data-stu-id="05653-104">SYNTAX</span></span>

### <span data-ttu-id="05653-105">ServiceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="05653-105">ServiceNameParameterSet (Default)</span></span>
```
Remove-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05653-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05653-106">InputObjectParameterSet</span></span>
```
Remove-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05653-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05653-107">ResourceIdParameterSet</span></span>
```
Remove-AzHealthcareApisService [-ResourceId] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05653-108">描述</span><span class="sxs-lookup"><span data-stu-id="05653-108">DESCRIPTION</span></span>
<span data-ttu-id="05653-109">刪除服務實例。</span><span class="sxs-lookup"><span data-stu-id="05653-109">Deletes a service instance.</span></span>

## <span data-ttu-id="05653-110">例子</span><span class="sxs-lookup"><span data-stu-id="05653-110">EXAMPLES</span></span>

### <span data-ttu-id="05653-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="05653-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup
```

<span data-ttu-id="05653-112">刪除提供的資源群組中提供之名稱的現有醫療保健發票服務。</span><span class="sxs-lookup"><span data-stu-id="05653-112">Deletes the existing HealthcareApis service with the provided name within a provided resource group.</span></span>

### <span data-ttu-id="05653-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="05653-113">Example 2</span></span>
```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService
PS C:\> Remove-AzHealthcareApisService -ResourceId $ResourceId
```

<span data-ttu-id="05653-114">刪除提供之 ResourceId 的現有醫療保健發票服務。</span><span class="sxs-lookup"><span data-stu-id="05653-114">Deletes the existing HealthcareApis service with the provided ResourceId.</span></span>

### <span data-ttu-id="05653-115">範例 3</span><span class="sxs-lookup"><span data-stu-id="05653-115">Example 3</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName MyResourceGroup -Name MyService | Remove-AzHealthcareApisService
```

<span data-ttu-id="05653-116">刪除提供的醫療保健發票服務物件。</span><span class="sxs-lookup"><span data-stu-id="05653-116">Deletes the provided HealthcareApis service object.</span></span>

## <span data-ttu-id="05653-117">參數</span><span class="sxs-lookup"><span data-stu-id="05653-117">PARAMETERS</span></span>

### <span data-ttu-id="05653-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05653-118">-AsJob</span></span>
<span data-ttu-id="05653-119">在背景中以工作執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05653-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="05653-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05653-120">-DefaultProfile</span></span>
<span data-ttu-id="05653-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="05653-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05653-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05653-122">-InputObject</span></span>
<span data-ttu-id="05653-123">醫療保健發票服務物件</span><span class="sxs-lookup"><span data-stu-id="05653-123">HealthcareApis service object</span></span>

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

### <span data-ttu-id="05653-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="05653-124">-Name</span></span>
<span data-ttu-id="05653-125">醫療保健發票服務名稱。</span><span class="sxs-lookup"><span data-stu-id="05653-125">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="05653-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05653-126">-PassThru</span></span>
<span data-ttu-id="05653-127">如果提供，如果作業成功，則會返回 True</span><span class="sxs-lookup"><span data-stu-id="05653-127">If provided, returns true if the operation was successful</span></span>

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

### <span data-ttu-id="05653-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05653-128">-ResourceGroupName</span></span>
<span data-ttu-id="05653-129">資源組名。</span><span class="sxs-lookup"><span data-stu-id="05653-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="05653-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05653-130">-ResourceId</span></span>
<span data-ttu-id="05653-131">HealthcareApis Service ResourceId.</span><span class="sxs-lookup"><span data-stu-id="05653-131">HealthcareApis Service ResourceId.</span></span>

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

### <span data-ttu-id="05653-132">-確認</span><span class="sxs-lookup"><span data-stu-id="05653-132">-Confirm</span></span>
<span data-ttu-id="05653-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="05653-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05653-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05653-134">-WhatIf</span></span>
<span data-ttu-id="05653-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="05653-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05653-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05653-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05653-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05653-137">CommonParameters</span></span>
<span data-ttu-id="05653-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="05653-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05653-139">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05653-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05653-140">輸入</span><span class="sxs-lookup"><span data-stu-id="05653-140">INPUTS</span></span>

### <span data-ttu-id="05653-141">Microsoft.Azure.Commands.HealthcareApis.models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="05653-141">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="05653-142">System.String</span><span class="sxs-lookup"><span data-stu-id="05653-142">System.String</span></span>

## <span data-ttu-id="05653-143">輸出</span><span class="sxs-lookup"><span data-stu-id="05653-143">OUTPUTS</span></span>

### <span data-ttu-id="05653-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="05653-144">System.Boolean</span></span>

## <span data-ttu-id="05653-145">筆記</span><span class="sxs-lookup"><span data-stu-id="05653-145">NOTES</span></span>

## <span data-ttu-id="05653-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="05653-146">RELATED LINKS</span></span>
