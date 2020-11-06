---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMChefExtension.md
ms.openlocfilehash: 8a64b97fb936daae2840392abe7dff8702207638
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613244"
---
# <span data-ttu-id="2f058-101">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="2f058-101">Remove-AzVMChefExtension</span></span>

## <span data-ttu-id="2f058-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2f058-102">SYNOPSIS</span></span>
<span data-ttu-id="2f058-103">從虛擬機器移除主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="2f058-103">Removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="2f058-104">句法</span><span class="sxs-lookup"><span data-stu-id="2f058-104">SYNTAX</span></span>

### <span data-ttu-id="2f058-105">Linux</span><span class="sxs-lookup"><span data-stu-id="2f058-105">Linux</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f058-106">時間</span><span class="sxs-lookup"><span data-stu-id="2f058-106">Windows</span></span>
```
Remove-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f058-107">說明</span><span class="sxs-lookup"><span data-stu-id="2f058-107">DESCRIPTION</span></span>
<span data-ttu-id="2f058-108">**AzVMChefExtension** Cmdlet 會從虛擬機器中移除主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="2f058-108">The **Remove-AzVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="2f058-109">示例</span><span class="sxs-lookup"><span data-stu-id="2f058-109">EXAMPLES</span></span>

### <span data-ttu-id="2f058-110">範例1：從 Windows 虛擬機器移除主廚延伸</span><span class="sxs-lookup"><span data-stu-id="2f058-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="2f058-111">這個命令會從以屬於名為 ResourceGroup001 之資源群組的名為 WindowsVM001 的 Windows 虛擬機器中移除主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="2f058-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="2f058-112">範例2：從 Linux 虛擬機器移除主廚擴充功能</span><span class="sxs-lookup"><span data-stu-id="2f058-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="2f058-113">這個命令會從以 Linux 為基礎的虛擬電腦（屬於名為 ResourceGroup002 的資源群組），移除名為 LinuxVM001 的主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="2f058-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="2f058-114">參數</span><span class="sxs-lookup"><span data-stu-id="2f058-114">PARAMETERS</span></span>

### <span data-ttu-id="2f058-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f058-115">-DefaultProfile</span></span>
<span data-ttu-id="2f058-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f058-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f058-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="2f058-117">-Linux</span></span>
<span data-ttu-id="2f058-118">表示此 Cmdlet 針對 Linux 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2f058-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

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

### <span data-ttu-id="2f058-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f058-119">-Name</span></span>
<span data-ttu-id="2f058-120">指定此 Cmdlet 移除之主廚延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f058-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2f058-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2f058-121">-NoWait</span></span>
<span data-ttu-id="2f058-122">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="2f058-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="2f058-123">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="2f058-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="2f058-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f058-124">-ResourceGroupName</span></span>
<span data-ttu-id="2f058-125">指定包含虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2f058-125">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="2f058-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="2f058-126">-VMName</span></span>
<span data-ttu-id="2f058-127">指定此 Cmdlet 移除主廚延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="2f058-127">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="2f058-128">-Windows</span><span class="sxs-lookup"><span data-stu-id="2f058-128">-Windows</span></span>
<span data-ttu-id="2f058-129">指示此 Cmdlet 針對 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2f058-129">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

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

### <span data-ttu-id="2f058-130">-確認</span><span class="sxs-lookup"><span data-stu-id="2f058-130">-Confirm</span></span>
<span data-ttu-id="2f058-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2f058-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f058-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f058-132">-WhatIf</span></span>
<span data-ttu-id="2f058-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2f058-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f058-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2f058-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f058-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f058-135">CommonParameters</span></span>
<span data-ttu-id="2f058-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2f058-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f058-137">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2f058-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f058-138">輸入</span><span class="sxs-lookup"><span data-stu-id="2f058-138">INPUTS</span></span>

### <span data-ttu-id="2f058-139">System.object</span><span class="sxs-lookup"><span data-stu-id="2f058-139">System.String</span></span>

## <span data-ttu-id="2f058-140">輸出</span><span class="sxs-lookup"><span data-stu-id="2f058-140">OUTPUTS</span></span>

### <span data-ttu-id="2f058-141">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="2f058-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2f058-142">筆記</span><span class="sxs-lookup"><span data-stu-id="2f058-142">NOTES</span></span>

## <span data-ttu-id="2f058-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f058-143">RELATED LINKS</span></span>

[<span data-ttu-id="2f058-144">AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="2f058-144">Get-AzVMChefExtension</span></span>](./Get-AzVMChefExtension.md)

[<span data-ttu-id="2f058-145">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="2f058-145">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)
