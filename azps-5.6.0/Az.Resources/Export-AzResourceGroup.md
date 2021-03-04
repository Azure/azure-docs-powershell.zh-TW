---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: 1f4f518cb203414392fe8d3f01fc0031be7f79e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907545"
---
# <span data-ttu-id="46d73-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="46d73-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="46d73-102">簡介</span><span class="sxs-lookup"><span data-stu-id="46d73-102">SYNOPSIS</span></span>
<span data-ttu-id="46d73-103">將資源群組捕獲為範本，並存到檔案中。</span><span class="sxs-lookup"><span data-stu-id="46d73-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="46d73-104">語法</span><span class="sxs-lookup"><span data-stu-id="46d73-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-SkipResourceNameParameterization] [-SkipAllParameterization] [-Resource <String[]>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46d73-105">描述</span><span class="sxs-lookup"><span data-stu-id="46d73-105">DESCRIPTION</span></span>
<span data-ttu-id="46d73-106">**Export-AzResourceGroup** Cmdlet 會將指定的資源群組視為範本，並存到 JSON 檔案。當您已在資源群組中建立一些資源，然後想要運用使用範本支援部署的好處時，這項功能就很實用。</span><span class="sxs-lookup"><span data-stu-id="46d73-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="46d73-107">此 Cmdlet 提供您一個簡單的起點，為資源群組中的現有資源產生範本。</span><span class="sxs-lookup"><span data-stu-id="46d73-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="46d73-108">在某些情況下，此 Cmdlet 無法產生範本的某些部分。</span><span class="sxs-lookup"><span data-stu-id="46d73-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="46d73-109">警告訊息會通知您資源失敗。</span><span class="sxs-lookup"><span data-stu-id="46d73-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="46d73-110">系統仍然會針對成功的部分產生範本。</span><span class="sxs-lookup"><span data-stu-id="46d73-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="46d73-111">例子</span><span class="sxs-lookup"><span data-stu-id="46d73-111">EXAMPLES</span></span>

### <span data-ttu-id="46d73-112">範例 1：匯出資源群組</span><span class="sxs-lookup"><span data-stu-id="46d73-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="46d73-113">此命令會將名為 TestGroup 的資源群組當做範本，並存到目前目錄中的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="46d73-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="46d73-114">範例 2：從資源群組匯出單一資源</span><span class="sxs-lookup"><span data-stu-id="46d73-114">Example 2: Export a single resource from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -Resource "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVirtualMachine"
```

<span data-ttu-id="46d73-115">此命令會從 "TestGroup" 資源群組中，將名為 "TestVirtualMachine" 的虛擬機器資源當做範本，並存到目前目錄中的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="46d73-115">This command captures the Virtual Machine resource named "TestVirtualMachine" from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="46d73-116">範例 3：從資源群組匯出資源選取範圍</span><span class="sxs-lookup"><span data-stu-id="46d73-116">Example 3: Export a selection of resources from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -SkipAllParameterization -Resource @(
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVm",
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Network/networkInterfaces/TestNic"
)
```

<span data-ttu-id="46d73-117">此命令會以範本從 「TestGroup」資源群組中捕獲兩個資源，並存到目前目錄中的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="46d73-117">This command captures two resources from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span> <span data-ttu-id="46d73-118">產生的範本不會包含任何產生的參數。</span><span class="sxs-lookup"><span data-stu-id="46d73-118">The generated template will not contain any generated parameters.</span></span>

## <span data-ttu-id="46d73-119">參數</span><span class="sxs-lookup"><span data-stu-id="46d73-119">PARAMETERS</span></span>

### <span data-ttu-id="46d73-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="46d73-120">-ApiVersion</span></span>
<span data-ttu-id="46d73-121">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="46d73-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="46d73-122">如果未指定，會使用最新的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="46d73-122">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="46d73-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46d73-123">-DefaultProfile</span></span>
<span data-ttu-id="46d73-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="46d73-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46d73-125">-強制</span><span class="sxs-lookup"><span data-stu-id="46d73-125">-Force</span></span>
<span data-ttu-id="46d73-126">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="46d73-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="46d73-127">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="46d73-127">-IncludeComments</span></span>
<span data-ttu-id="46d73-128">表示此作業會匯出包含批註的範本。</span><span class="sxs-lookup"><span data-stu-id="46d73-128">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="46d73-129">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="46d73-129">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="46d73-130">表示此作業會匯出具有預設值的範本參數。</span><span class="sxs-lookup"><span data-stu-id="46d73-130">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="46d73-131">-路徑</span><span class="sxs-lookup"><span data-stu-id="46d73-131">-Path</span></span>
<span data-ttu-id="46d73-132">指定範本檔案的輸出路徑。</span><span class="sxs-lookup"><span data-stu-id="46d73-132">Specifies the output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46d73-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="46d73-133">-Pre</span></span>
<span data-ttu-id="46d73-134">表示此 Cmdlet 會在自動決定要使用哪個 API 版本時，使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="46d73-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="46d73-135">-資源</span><span class="sxs-lookup"><span data-stu-id="46d73-135">-Resource</span></span>
<span data-ttu-id="46d73-136">這是要篩選結果的資源Id 清單。</span><span class="sxs-lookup"><span data-stu-id="46d73-136">A list of resourceIds to filter the results by.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d73-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46d73-137">-ResourceGroupName</span></span>
<span data-ttu-id="46d73-138">指定要匯出的資源組名。</span><span class="sxs-lookup"><span data-stu-id="46d73-138">Specifies the name of the resource group to export.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46d73-139">-SkipAllParameterization</span><span class="sxs-lookup"><span data-stu-id="46d73-139">-SkipAllParameterization</span></span>
<span data-ttu-id="46d73-140">略過所有參數化。</span><span class="sxs-lookup"><span data-stu-id="46d73-140">Skip all parameterization.</span></span>

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

### <span data-ttu-id="46d73-141">-SkipResourceNameParameterization</span><span class="sxs-lookup"><span data-stu-id="46d73-141">-SkipResourceNameParameterization</span></span>
<span data-ttu-id="46d73-142">略過資源名稱參數化。</span><span class="sxs-lookup"><span data-stu-id="46d73-142">Skip resource name parameterization.</span></span>

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

### <span data-ttu-id="46d73-143">-確認</span><span class="sxs-lookup"><span data-stu-id="46d73-143">-Confirm</span></span>
<span data-ttu-id="46d73-144">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="46d73-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d73-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46d73-145">-WhatIf</span></span>
<span data-ttu-id="46d73-146">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="46d73-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46d73-147">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="46d73-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46d73-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d73-148">CommonParameters</span></span>
<span data-ttu-id="46d73-149">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="46d73-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d73-150">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46d73-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d73-151">輸入</span><span class="sxs-lookup"><span data-stu-id="46d73-151">INPUTS</span></span>

### <span data-ttu-id="46d73-152">System.String</span><span class="sxs-lookup"><span data-stu-id="46d73-152">System.String</span></span>

## <span data-ttu-id="46d73-153">輸出</span><span class="sxs-lookup"><span data-stu-id="46d73-153">OUTPUTS</span></span>

### <span data-ttu-id="46d73-154">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="46d73-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="46d73-155">筆記</span><span class="sxs-lookup"><span data-stu-id="46d73-155">NOTES</span></span>

## <span data-ttu-id="46d73-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="46d73-156">RELATED LINKS</span></span>

[<span data-ttu-id="46d73-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="46d73-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


