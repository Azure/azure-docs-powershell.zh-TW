---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: 74605a57ab3f2c0898bf3eeb80950f86d4f65d94
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285988"
---
# <span data-ttu-id="4b125-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4b125-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="4b125-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4b125-102">SYNOPSIS</span></span>
<span data-ttu-id="4b125-103">將資源群組捕獲為範本，並將它儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="4b125-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="4b125-104">句法</span><span class="sxs-lookup"><span data-stu-id="4b125-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-SkipResourceNameParameterization] [-SkipAllParameterization] [-Resource <String[]>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4b125-105">說明</span><span class="sxs-lookup"><span data-stu-id="4b125-105">DESCRIPTION</span></span>
<span data-ttu-id="4b125-106">**Export AzResourceGroup** Cmdlet 會將指定的資源群組捕獲為範本，並將其儲存至 JSON 檔案。這在您已在資源群組中建立一些資源，然後想要利用範本支援的好處的情況下，可能會很有用。</span><span class="sxs-lookup"><span data-stu-id="4b125-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="4b125-107">這個 Cmdlet 能讓您輕鬆地開始為 [資源] 群組中現有的資源產生範本。</span><span class="sxs-lookup"><span data-stu-id="4b125-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="4b125-108">在某些情況下，這個 Cmdlet 無法產生範本的某些部分。</span><span class="sxs-lookup"><span data-stu-id="4b125-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="4b125-109">警告訊息會告知您失敗的資源。</span><span class="sxs-lookup"><span data-stu-id="4b125-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="4b125-110">您仍會針對成功的元件產生範本。</span><span class="sxs-lookup"><span data-stu-id="4b125-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="4b125-111">示例</span><span class="sxs-lookup"><span data-stu-id="4b125-111">EXAMPLES</span></span>

### <span data-ttu-id="4b125-112">範例1：匯出資源群組</span><span class="sxs-lookup"><span data-stu-id="4b125-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="4b125-113">這個命令會將名為 TestGroup 的資源群組捕獲為範本，並將它儲存到目前目錄中的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="4b125-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="4b125-114">範例2：從資源群組匯出單一資源</span><span class="sxs-lookup"><span data-stu-id="4b125-114">Example 2: Export a single resource from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -Resource "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVirtualMachine"
```

<span data-ttu-id="4b125-115">這個命令會從「TestGroup」資源群組捕獲名為「TestVirtualMachine」的虛擬機器資源做為範本，並將它儲存到目前目錄中的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="4b125-115">This command captures the Virtual Machine resource named "TestVirtualMachine" from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="4b125-116">範例3：從資源群組匯出資源的選取範圍</span><span class="sxs-lookup"><span data-stu-id="4b125-116">Example 3: Export a selection of resources from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -SkipAllParameterization -Resource @(
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVm",
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Network/networkInterfaces/TestNic"
)
```

<span data-ttu-id="4b125-117">這個命令會將「TestGroup」資源群組中的兩個資源捕獲為範本，並將它儲存到目前目錄中的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="4b125-117">This command captures two resources from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span> <span data-ttu-id="4b125-118">產生的範本不會包含任何產生的參數。</span><span class="sxs-lookup"><span data-stu-id="4b125-118">The generated template will not contain any generated parameters.</span></span>

## <span data-ttu-id="4b125-119">參數</span><span class="sxs-lookup"><span data-stu-id="4b125-119">PARAMETERS</span></span>

### <span data-ttu-id="4b125-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4b125-120">-ApiVersion</span></span>
<span data-ttu-id="4b125-121">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="4b125-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4b125-122">如果沒有指定，則會使用最新的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="4b125-122">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="4b125-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b125-123">-DefaultProfile</span></span>
<span data-ttu-id="4b125-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4b125-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b125-125">-Force</span><span class="sxs-lookup"><span data-stu-id="4b125-125">-Force</span></span>
<span data-ttu-id="4b125-126">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="4b125-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4b125-127">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="4b125-127">-IncludeComments</span></span>
<span data-ttu-id="4b125-128">指示這個作業會將範本匯出為批註。</span><span class="sxs-lookup"><span data-stu-id="4b125-128">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="4b125-129">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="4b125-129">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="4b125-130">指示此操作會匯出具有預設值的範本參數。</span><span class="sxs-lookup"><span data-stu-id="4b125-130">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="4b125-131">-Path</span><span class="sxs-lookup"><span data-stu-id="4b125-131">-Path</span></span>
<span data-ttu-id="4b125-132">指定範本檔案的輸出路徑。</span><span class="sxs-lookup"><span data-stu-id="4b125-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="4b125-133">-預先</span><span class="sxs-lookup"><span data-stu-id="4b125-133">-Pre</span></span>
<span data-ttu-id="4b125-134">表示當您自動判斷要使用哪個 API 版本時，此 Cmdlet 會使用預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="4b125-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="4b125-135">-資源</span><span class="sxs-lookup"><span data-stu-id="4b125-135">-Resource</span></span>
<span data-ttu-id="4b125-136">篩選結果的 resourceIds 清單。</span><span class="sxs-lookup"><span data-stu-id="4b125-136">A list of resourceIds to filter the results by.</span></span>

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

### <span data-ttu-id="4b125-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b125-137">-ResourceGroupName</span></span>
<span data-ttu-id="4b125-138">指定要匯出之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b125-138">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="4b125-139">-SkipAllParameterization</span><span class="sxs-lookup"><span data-stu-id="4b125-139">-SkipAllParameterization</span></span>
<span data-ttu-id="4b125-140">略過所有參數化。</span><span class="sxs-lookup"><span data-stu-id="4b125-140">Skip all parameterization.</span></span>

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

### <span data-ttu-id="4b125-141">-SkipResourceNameParameterization</span><span class="sxs-lookup"><span data-stu-id="4b125-141">-SkipResourceNameParameterization</span></span>
<span data-ttu-id="4b125-142">略過資源名稱參數化。</span><span class="sxs-lookup"><span data-stu-id="4b125-142">Skip resource name parameterization.</span></span>

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

### <span data-ttu-id="4b125-143">-確認</span><span class="sxs-lookup"><span data-stu-id="4b125-143">-Confirm</span></span>
<span data-ttu-id="4b125-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4b125-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b125-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b125-145">-WhatIf</span></span>
<span data-ttu-id="4b125-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4b125-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b125-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4b125-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b125-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b125-148">CommonParameters</span></span>
<span data-ttu-id="4b125-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4b125-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b125-150">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4b125-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b125-151">輸入</span><span class="sxs-lookup"><span data-stu-id="4b125-151">INPUTS</span></span>

### <span data-ttu-id="4b125-152">System.object</span><span class="sxs-lookup"><span data-stu-id="4b125-152">System.String</span></span>

## <span data-ttu-id="4b125-153">輸出</span><span class="sxs-lookup"><span data-stu-id="4b125-153">OUTPUTS</span></span>

### <span data-ttu-id="4b125-154">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="4b125-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4b125-155">筆記</span><span class="sxs-lookup"><span data-stu-id="4b125-155">NOTES</span></span>

## <span data-ttu-id="4b125-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b125-156">RELATED LINKS</span></span>

[<span data-ttu-id="4b125-157">AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4b125-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


