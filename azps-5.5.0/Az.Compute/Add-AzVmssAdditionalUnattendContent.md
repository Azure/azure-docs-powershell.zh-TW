---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9BE2E42C-594B-4B67-866C-BBA3B84AA5FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssAdditionalUnattendContent.md
ms.openlocfilehash: 051228464b2f1e9770507ceacd4eaabfce5236b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127906"
---
# <span data-ttu-id="d3ec2-101">Add-AzVmssAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="d3ec2-101">Add-AzVmssAdditionalUnattendContent</span></span>

## <span data-ttu-id="d3ec2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d3ec2-102">SYNOPSIS</span></span>
<span data-ttu-id="d3ec2-103">將資訊新增至無人參與的 Windows 安裝程式應答檔。</span><span class="sxs-lookup"><span data-stu-id="d3ec2-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="d3ec2-104">句法</span><span class="sxs-lookup"><span data-stu-id="d3ec2-104">SYNTAX</span></span>

```
Add-AzVmssAdditionalUnattendContent [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-PassName] <PassNames>] [[-ComponentName] <ComponentNames>] [[-SettingName] <SettingNames>]
 [[-Content] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3ec2-105">說明</span><span class="sxs-lookup"><span data-stu-id="d3ec2-105">DESCRIPTION</span></span>
<span data-ttu-id="d3ec2-106">**AzVmssAdditionalUnattendContent** Cmdlet 會將資訊新增到無人參與的 Windows 安裝程式應答檔案。</span><span class="sxs-lookup"><span data-stu-id="d3ec2-106">The **Add-AzVmssAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="d3ec2-107">示例</span><span class="sxs-lookup"><span data-stu-id="d3ec2-107">EXAMPLES</span></span>

### <span data-ttu-id="d3ec2-108">範例1：將資訊新增至無人參與的 Windows 安裝程式應答檔</span><span class="sxs-lookup"><span data-stu-id="d3ec2-108">Example 1: Add information to the unattended Windows Setup answer file</span></span>
```
PS C:\> Add-AzVmssAdditionalUnattendContent -VirtualMachineScaleSet $VMSS -ComponentName  $AUCComponentName -Content  $AUCContent -PassName $AUCPassName -SettingName  $AUCSetting
```

<span data-ttu-id="d3ec2-109">這個命令會將資訊新增到無人參與的 Windows 安裝程式應答檔案。</span><span class="sxs-lookup"><span data-stu-id="d3ec2-109">This command adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="d3ec2-110">參數</span><span class="sxs-lookup"><span data-stu-id="d3ec2-110">PARAMETERS</span></span>

### <span data-ttu-id="d3ec2-111">-ComponentName</span><span class="sxs-lookup"><span data-stu-id="d3ec2-111">-ComponentName</span></span>
<span data-ttu-id="d3ec2-112">指定要使用已新增內容進行設定的元件名稱。</span><span class="sxs-lookup"><span data-stu-id="d3ec2-112">Specifies the name of the component to configure with the added content.</span></span>
<span data-ttu-id="d3ec2-113">唯一允許的值為 Microsoft-Windows-Shell-Setup。</span><span class="sxs-lookup"><span data-stu-id="d3ec2-113">The only allowable value is Microsoft-Windows-Shell-Setup.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ComponentNames]
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftWindowsShellSetup

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3ec2-114">-內容</span><span class="sxs-lookup"><span data-stu-id="d3ec2-114">-Content</span></span>
<span data-ttu-id="d3ec2-115">指定要新增至指定路徑和元件之 unattend.xml 檔案之 XML 格式的內容。</span><span class="sxs-lookup"><span data-stu-id="d3ec2-115">Specifies the XML formatted content that is added to the unattend.xml file for the specified path and component.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3ec2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3ec2-116">-DefaultProfile</span></span>
<span data-ttu-id="d3ec2-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d3ec2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3ec2-118">-PassName</span><span class="sxs-lookup"><span data-stu-id="d3ec2-118">-PassName</span></span>
<span data-ttu-id="d3ec2-119">指定內容適用之階段的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3ec2-119">Specifies the name of the pass that the content applies to.</span></span>
<span data-ttu-id="d3ec2-120">唯一允許的值為 oobeSystem。</span><span class="sxs-lookup"><span data-stu-id="d3ec2-120">The only allowable value is oobeSystem.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.PassNames]
Parameter Sets: (All)
Aliases:
Accepted values: OobeSystem

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3ec2-121">-SettingName</span><span class="sxs-lookup"><span data-stu-id="d3ec2-121">-SettingName</span></span>
<span data-ttu-id="d3ec2-122">指定要套用內容的設定名稱。</span><span class="sxs-lookup"><span data-stu-id="d3ec2-122">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="d3ec2-123">此參數可接受的值為：：</span><span class="sxs-lookup"><span data-stu-id="d3ec2-123">The acceptable values for this parameter are::</span></span>
- <span data-ttu-id="d3ec2-124">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="d3ec2-124">FirstLogonCommands</span></span>
- <span data-ttu-id="d3ec2-125">自動</span><span class="sxs-lookup"><span data-stu-id="d3ec2-125">AutoLogon</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3ec2-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d3ec2-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d3ec2-127">指定虛擬機器 **縮放集** 物件。</span><span class="sxs-lookup"><span data-stu-id="d3ec2-127">Specify the virtual machine **Scale Set** object.</span></span>
<span data-ttu-id="d3ec2-128">您可以使用 [新的-AzVmssConfig](./New-AzVmssConfig.md) Cmdlet 來建立物件。</span><span class="sxs-lookup"><span data-stu-id="d3ec2-128">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3ec2-129">-確認</span><span class="sxs-lookup"><span data-stu-id="d3ec2-129">-Confirm</span></span>
<span data-ttu-id="d3ec2-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d3ec2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3ec2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3ec2-131">-WhatIf</span></span>
<span data-ttu-id="d3ec2-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d3ec2-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3ec2-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d3ec2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3ec2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3ec2-134">CommonParameters</span></span>
<span data-ttu-id="d3ec2-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d3ec2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3ec2-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d3ec2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3ec2-137">輸入</span><span class="sxs-lookup"><span data-stu-id="d3ec2-137">INPUTS</span></span>

### <span data-ttu-id="d3ec2-138">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="d3ec2-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="d3ec2-139">"PassNames" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="d3ec2-139">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.PassNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d3ec2-140">"ComponentNames" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="d3ec2-140">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ComponentNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d3ec2-141">"SettingNames" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="d3ec2-141">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="d3ec2-142">System.object</span><span class="sxs-lookup"><span data-stu-id="d3ec2-142">System.String</span></span>

## <span data-ttu-id="d3ec2-143">輸出</span><span class="sxs-lookup"><span data-stu-id="d3ec2-143">OUTPUTS</span></span>

### <span data-ttu-id="d3ec2-144">PSVirtualMachineScaleSet 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="d3ec2-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="d3ec2-145">筆記</span><span class="sxs-lookup"><span data-stu-id="d3ec2-145">NOTES</span></span>

## <span data-ttu-id="d3ec2-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="d3ec2-146">RELATED LINKS</span></span>

[<span data-ttu-id="d3ec2-147">新-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d3ec2-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
