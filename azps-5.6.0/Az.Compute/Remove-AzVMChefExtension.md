---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 56973d23e59a3d34b2caadce3677ca0bfd5f3c5e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907150"
---
# <span data-ttu-id="e3bf5-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="e3bf5-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="e3bf5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e3bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="e3bf5-103">移除虛擬機器的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="e3bf5-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="e3bf5-104">語法</span><span class="sxs-lookup"><span data-stu-id="e3bf5-104">SYNTAX</span></span>

### <span data-ttu-id="e3bf5-105">Linux</span><span class="sxs-lookup"><span data-stu-id="e3bf5-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3bf5-106">窗戶</span><span class="sxs-lookup"><span data-stu-id="e3bf5-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3bf5-107">描述</span><span class="sxs-lookup"><span data-stu-id="e3bf5-107">DESCRIPTION</span></span>
<span data-ttu-id="e3bf5-108">**Remove-Az VIRTUALChefExtension** Cmdlet 會從虛擬機器移除一個副檔名。。</span><span class="sxs-lookup"><span data-stu-id="e3bf5-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="e3bf5-109">例子</span><span class="sxs-lookup"><span data-stu-id="e3bf5-109">EXAMPLES</span></span>

### <span data-ttu-id="e3bf5-110">範例 1：從 Windows 虛擬機器移除擴充功能</span><span class="sxs-lookup"><span data-stu-id="e3bf5-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="e3bf5-111">此命令會從 Windows 型虛擬機器中，移除名稱為 Windows MACHINE001 的擴充功能，該虛擬機器屬於名為 ResourceGroup001 的資源群組。</span><span class="sxs-lookup"><span data-stu-id="e3bf5-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="e3bf5-112">範例 2：從 Linux 虛擬機器移除擴充功能</span><span class="sxs-lookup"><span data-stu-id="e3bf5-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="e3bf5-113">此命令會從名為 Linux LINUX LINUX0001 的 Linux 虛擬機器移除一個名稱為 ResourceGroup002 的資源群組的一個擴充程式。</span><span class="sxs-lookup"><span data-stu-id="e3bf5-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="e3bf5-114">參數</span><span class="sxs-lookup"><span data-stu-id="e3bf5-114">PARAMETERS</span></span>

### <span data-ttu-id="e3bf5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3bf5-115">-DefaultProfile</span></span>
<span data-ttu-id="e3bf5-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3bf5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3bf5-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="e3bf5-117">-Linux</span></span>
<span data-ttu-id="e3bf5-118">表示此 Cmdlet 會以 Linux 虛擬機器為目標。</span><span class="sxs-lookup"><span data-stu-id="e3bf5-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3bf5-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3bf5-119">-Name</span></span>
<span data-ttu-id="e3bf5-120">指定此 Cmdlet 移除的擴充功能名稱。</span><span class="sxs-lookup"><span data-stu-id="e3bf5-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3bf5-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e3bf5-121">-NoWait</span></span>
<span data-ttu-id="e3bf5-122">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="e3bf5-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="e3bf5-123">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="e3bf5-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="e3bf5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3bf5-124">-ResourceGroupName</span></span>
<span data-ttu-id="e3bf5-125">指定包含虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e3bf5-125">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3bf5-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="e3bf5-126">-VMName</span></span>
<span data-ttu-id="e3bf5-127">指定此 Cmdlet 會移除擴充名的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="e3bf5-127">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3bf5-128">-Windows</span><span class="sxs-lookup"><span data-stu-id="e3bf5-128">-Windows</span></span>
<span data-ttu-id="e3bf5-129">表示此 Cmdlet 會以 Windows 虛擬機器為目標。</span><span class="sxs-lookup"><span data-stu-id="e3bf5-129">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3bf5-130">-確認</span><span class="sxs-lookup"><span data-stu-id="e3bf5-130">-Confirm</span></span>
<span data-ttu-id="e3bf5-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e3bf5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3bf5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3bf5-132">-WhatIf</span></span>
<span data-ttu-id="e3bf5-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e3bf5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3bf5-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e3bf5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3bf5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3bf5-135">CommonParameters</span></span>
<span data-ttu-id="e3bf5-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e3bf5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3bf5-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3bf5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3bf5-138">輸入</span><span class="sxs-lookup"><span data-stu-id="e3bf5-138">INPUTS</span></span>

### <span data-ttu-id="e3bf5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e3bf5-139">System.String</span></span>

## <span data-ttu-id="e3bf5-140">輸出</span><span class="sxs-lookup"><span data-stu-id="e3bf5-140">OUTPUTS</span></span>

### <span data-ttu-id="e3bf5-141">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e3bf5-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e3bf5-142">筆記</span><span class="sxs-lookup"><span data-stu-id="e3bf5-142">NOTES</span></span>

## <span data-ttu-id="e3bf5-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3bf5-143">RELATED LINKS</span></span>

[<span data-ttu-id="e3bf5-144">Get-AzEVChefExtension</span><span class="sxs-lookup"><span data-stu-id="e3bf5-144">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="e3bf5-145">Set-AzEVChefExtension</span><span class="sxs-lookup"><span data-stu-id="e3bf5-145">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
