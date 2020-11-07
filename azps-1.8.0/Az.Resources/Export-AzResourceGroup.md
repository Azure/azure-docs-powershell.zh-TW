---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: f1801aab91887b3dd0d6a9842c7d4a6de1988a88
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93626672"
---
# <span data-ttu-id="650dd-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="650dd-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="650dd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="650dd-102">SYNOPSIS</span></span>
<span data-ttu-id="650dd-103">將資源群組捕獲為範本，並將它儲存至檔案。</span><span class="sxs-lookup"><span data-stu-id="650dd-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="650dd-104">句法</span><span class="sxs-lookup"><span data-stu-id="650dd-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="650dd-105">說明</span><span class="sxs-lookup"><span data-stu-id="650dd-105">DESCRIPTION</span></span>
<span data-ttu-id="650dd-106">**Export AzResourceGroup** Cmdlet 會將指定的資源群組捕獲為範本，並將其儲存至 JSON 檔案。這在您已在資源群組中建立一些資源，然後想要利用範本支援的好處的情況下，可能會很有用。</span><span class="sxs-lookup"><span data-stu-id="650dd-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="650dd-107">這個 Cmdlet 能讓您輕鬆地開始為 [資源] 群組中現有的資源產生範本。</span><span class="sxs-lookup"><span data-stu-id="650dd-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="650dd-108">在某些情況下，這個 Cmdlet 無法產生範本的某些部分。</span><span class="sxs-lookup"><span data-stu-id="650dd-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="650dd-109">警告訊息會告知您失敗的資源。</span><span class="sxs-lookup"><span data-stu-id="650dd-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="650dd-110">您仍會針對成功的元件產生範本。</span><span class="sxs-lookup"><span data-stu-id="650dd-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="650dd-111">示例</span><span class="sxs-lookup"><span data-stu-id="650dd-111">EXAMPLES</span></span>

### <span data-ttu-id="650dd-112">範例1：匯出資源群組</span><span class="sxs-lookup"><span data-stu-id="650dd-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="650dd-113">這個命令會將名為 TestGroup 的資源群組捕獲為範本，並將它儲存到目前目錄中的 JSON 檔案。</span><span class="sxs-lookup"><span data-stu-id="650dd-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="650dd-114">參數</span><span class="sxs-lookup"><span data-stu-id="650dd-114">PARAMETERS</span></span>

### <span data-ttu-id="650dd-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="650dd-115">-ApiVersion</span></span>
<span data-ttu-id="650dd-116">指定要使用的資源提供者 API 版本。</span><span class="sxs-lookup"><span data-stu-id="650dd-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="650dd-117">如果沒有指定，則會使用最新的 API 版本。</span><span class="sxs-lookup"><span data-stu-id="650dd-117">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="650dd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="650dd-118">-DefaultProfile</span></span>
<span data-ttu-id="650dd-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="650dd-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="650dd-120">-Force</span><span class="sxs-lookup"><span data-stu-id="650dd-120">-Force</span></span>
<span data-ttu-id="650dd-121">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="650dd-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="650dd-122">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="650dd-122">-IncludeComments</span></span>
<span data-ttu-id="650dd-123">指示這個作業會將範本匯出為批註。</span><span class="sxs-lookup"><span data-stu-id="650dd-123">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="650dd-124">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="650dd-124">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="650dd-125">指示此操作會匯出具有預設值的範本參數。</span><span class="sxs-lookup"><span data-stu-id="650dd-125">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="650dd-126">-Path</span><span class="sxs-lookup"><span data-stu-id="650dd-126">-Path</span></span>
<span data-ttu-id="650dd-127">指定範本檔案的輸出路徑。</span><span class="sxs-lookup"><span data-stu-id="650dd-127">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="650dd-128">-預先</span><span class="sxs-lookup"><span data-stu-id="650dd-128">-Pre</span></span>
<span data-ttu-id="650dd-129">表示當您自動判斷要使用哪個 API 版本時，此 Cmdlet 會使用預發行 API 版本。</span><span class="sxs-lookup"><span data-stu-id="650dd-129">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="650dd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="650dd-130">-ResourceGroupName</span></span>
<span data-ttu-id="650dd-131">指定要匯出之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="650dd-131">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="650dd-132">-確認</span><span class="sxs-lookup"><span data-stu-id="650dd-132">-Confirm</span></span>
<span data-ttu-id="650dd-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="650dd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="650dd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="650dd-134">-WhatIf</span></span>
<span data-ttu-id="650dd-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="650dd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="650dd-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="650dd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="650dd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="650dd-137">CommonParameters</span></span>
<span data-ttu-id="650dd-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="650dd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="650dd-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="650dd-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="650dd-140">輸入</span><span class="sxs-lookup"><span data-stu-id="650dd-140">INPUTS</span></span>

### <span data-ttu-id="650dd-141">System.object</span><span class="sxs-lookup"><span data-stu-id="650dd-141">System.String</span></span>

## <span data-ttu-id="650dd-142">輸出</span><span class="sxs-lookup"><span data-stu-id="650dd-142">OUTPUTS</span></span>

### <span data-ttu-id="650dd-143">系統管理. PSObject</span><span class="sxs-lookup"><span data-stu-id="650dd-143">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="650dd-144">筆記</span><span class="sxs-lookup"><span data-stu-id="650dd-144">NOTES</span></span>

## <span data-ttu-id="650dd-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="650dd-145">RELATED LINKS</span></span>

[<span data-ttu-id="650dd-146">AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="650dd-146">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


