---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmchefextension
schema: 2.0.0
ms.openlocfilehash: bc8dbd023d8730922614f749f540d182c63237a4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801705"
---
# <span data-ttu-id="4aff1-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="4aff1-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="4aff1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4aff1-102">SYNOPSIS</span></span>
<span data-ttu-id="4aff1-103">從虛擬機器移除主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="4aff1-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4aff1-104">句法</span><span class="sxs-lookup"><span data-stu-id="4aff1-104">SYNTAX</span></span>

### <span data-ttu-id="4aff1-105">Linux</span><span class="sxs-lookup"><span data-stu-id="4aff1-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4aff1-106">時間</span><span class="sxs-lookup"><span data-stu-id="4aff1-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4aff1-107">說明</span><span class="sxs-lookup"><span data-stu-id="4aff1-107">DESCRIPTION</span></span>
<span data-ttu-id="4aff1-108">**AzureVMChefExtension** Cmdlet 會從虛擬機器中移除主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="4aff1-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="4aff1-109">示例</span><span class="sxs-lookup"><span data-stu-id="4aff1-109">EXAMPLES</span></span>

### <span data-ttu-id="4aff1-110">範例1：從 Windows 虛擬機器移除主廚延伸</span><span class="sxs-lookup"><span data-stu-id="4aff1-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="4aff1-111">這個命令會從以屬於名為 ResourceGroup001 之資源群組的名為 WindowsVM001 的 Windows 虛擬機器中移除主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="4aff1-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="4aff1-112">範例2：從 Linux 虛擬機器移除主廚擴充功能</span><span class="sxs-lookup"><span data-stu-id="4aff1-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="4aff1-113">這個命令會從以 Linux 為基礎的虛擬電腦（屬於名為 ResourceGroup002 的資源群組），移除名為 LinuxVM001 的主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="4aff1-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="4aff1-114">參數</span><span class="sxs-lookup"><span data-stu-id="4aff1-114">PARAMETERS</span></span>

### <span data-ttu-id="4aff1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aff1-115">-DefaultProfile</span></span>
<span data-ttu-id="4aff1-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4aff1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aff1-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="4aff1-117">-Linux</span></span>
<span data-ttu-id="4aff1-118">表示此 Cmdlet 針對 Linux 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="4aff1-118">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aff1-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="4aff1-119">-Name</span></span>
<span data-ttu-id="4aff1-120">指定此 Cmdlet 移除之主廚延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="4aff1-120">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aff1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4aff1-121">-ResourceGroupName</span></span>
<span data-ttu-id="4aff1-122">指定包含虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4aff1-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aff1-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="4aff1-123">-VMName</span></span>
<span data-ttu-id="4aff1-124">指定此 Cmdlet 移除主廚延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="4aff1-124">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aff1-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="4aff1-125">-Windows</span></span>
<span data-ttu-id="4aff1-126">指示此 Cmdlet 針對 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="4aff1-126">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aff1-127">-確認</span><span class="sxs-lookup"><span data-stu-id="4aff1-127">-Confirm</span></span>
<span data-ttu-id="4aff1-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4aff1-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aff1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aff1-129">-WhatIf</span></span>
<span data-ttu-id="4aff1-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4aff1-130">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="4aff1-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4aff1-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aff1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aff1-132">CommonParameters</span></span>
<span data-ttu-id="4aff1-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4aff1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aff1-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4aff1-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aff1-135">輸入</span><span class="sxs-lookup"><span data-stu-id="4aff1-135">INPUTS</span></span>

### <span data-ttu-id="4aff1-136">所有</span><span class="sxs-lookup"><span data-stu-id="4aff1-136">None</span></span>
<span data-ttu-id="4aff1-137">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="4aff1-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4aff1-138">輸出</span><span class="sxs-lookup"><span data-stu-id="4aff1-138">OUTPUTS</span></span>

### <span data-ttu-id="4aff1-139">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="4aff1-139">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="4aff1-140">筆記</span><span class="sxs-lookup"><span data-stu-id="4aff1-140">NOTES</span></span>

## <span data-ttu-id="4aff1-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="4aff1-141">RELATED LINKS</span></span>

[<span data-ttu-id="4aff1-142">AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="4aff1-142">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="4aff1-143">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="4aff1-143">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)
