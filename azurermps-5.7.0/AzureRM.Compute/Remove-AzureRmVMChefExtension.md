---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 473C71A8-1DF7-487A-B239-B80E2BB63B82
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMChefExtension.md
ms.openlocfilehash: dc2e22acf8efd18a565c1ede7ff22aeb21679a47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448739"
---
# <span data-ttu-id="c3788-101">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="c3788-101">Remove-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="c3788-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3788-102">SYNOPSIS</span></span>
<span data-ttu-id="c3788-103">從虛擬機器移除主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="c3788-103">Removes the Chef extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3788-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3788-104">SYNTAX</span></span>

### <span data-ttu-id="c3788-105">Linux</span><span class="sxs-lookup"><span data-stu-id="c3788-105">Linux</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Linux]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3788-106">時間</span><span class="sxs-lookup"><span data-stu-id="c3788-106">Windows</span></span>
```
Remove-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Windows]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3788-107">說明</span><span class="sxs-lookup"><span data-stu-id="c3788-107">DESCRIPTION</span></span>
<span data-ttu-id="c3788-108">**AzureVMChefExtension** Cmdlet 會從虛擬機器中移除主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="c3788-108">The **Remove-AzureVMChefExtension** cmdlet removes the Chef extension from a virtual machine.</span></span>

## <span data-ttu-id="c3788-109">示例</span><span class="sxs-lookup"><span data-stu-id="c3788-109">EXAMPLES</span></span>

### <span data-ttu-id="c3788-110">範例1：從 Windows 虛擬機器移除主廚延伸</span><span class="sxs-lookup"><span data-stu-id="c3788-110">Example 1: Remove a Chef extension from a Windows virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="c3788-111">這個命令會從以屬於名為 ResourceGroup001 之資源群組的名為 WindowsVM001 的 Windows 虛擬機器中移除主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="c3788-111">This command removes a Chef extension from a Windows based virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="c3788-112">範例2：從 Linux 虛擬機器移除主廚擴充功能</span><span class="sxs-lookup"><span data-stu-id="c3788-112">Example 2: Remove a Chef extension from a Linux virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="c3788-113">這個命令會從以 Linux 為基礎的虛擬電腦（屬於名為 ResourceGroup002 的資源群組），移除名為 LinuxVM001 的主廚延伸。</span><span class="sxs-lookup"><span data-stu-id="c3788-113">This command removes a Chef extension from a Linux based virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="c3788-114">參數</span><span class="sxs-lookup"><span data-stu-id="c3788-114">PARAMETERS</span></span>

### <span data-ttu-id="c3788-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="c3788-115">-Linux</span></span>
<span data-ttu-id="c3788-116">表示此 Cmdlet 針對 Linux 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c3788-116">Indicates that this cmdlet targets a Linux virtual machine.</span></span>

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

### <span data-ttu-id="c3788-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="c3788-117">-Name</span></span>
<span data-ttu-id="c3788-118">指定此 Cmdlet 移除之主廚延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3788-118">Specifies the name of the Chef extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c3788-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3788-119">-ResourceGroupName</span></span>
<span data-ttu-id="c3788-120">指定包含虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3788-120">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="c3788-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="c3788-121">-VMName</span></span>
<span data-ttu-id="c3788-122">指定此 Cmdlet 移除主廚延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="c3788-122">Specifies the name of a virtual machine for which this cmdlet removes the Chef extension.</span></span>

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

### <span data-ttu-id="c3788-123">-Windows</span><span class="sxs-lookup"><span data-stu-id="c3788-123">-Windows</span></span>
<span data-ttu-id="c3788-124">指示此 Cmdlet 針對 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="c3788-124">Indicates that this cmdlet targets a Windows virtual machine.</span></span>

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

### <span data-ttu-id="c3788-125">-確認</span><span class="sxs-lookup"><span data-stu-id="c3788-125">-Confirm</span></span>
<span data-ttu-id="c3788-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c3788-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3788-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3788-127">-WhatIf</span></span>
<span data-ttu-id="c3788-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c3788-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="c3788-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3788-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3788-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3788-130">CommonParameters</span></span>
<span data-ttu-id="c3788-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3788-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3788-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c3788-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3788-133">輸入</span><span class="sxs-lookup"><span data-stu-id="c3788-133">INPUTS</span></span>

### <span data-ttu-id="c3788-134">所有</span><span class="sxs-lookup"><span data-stu-id="c3788-134">None</span></span>
<span data-ttu-id="c3788-135">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c3788-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c3788-136">輸出</span><span class="sxs-lookup"><span data-stu-id="c3788-136">OUTPUTS</span></span>

## <span data-ttu-id="c3788-137">筆記</span><span class="sxs-lookup"><span data-stu-id="c3788-137">NOTES</span></span>

## <span data-ttu-id="c3788-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3788-138">RELATED LINKS</span></span>

[<span data-ttu-id="c3788-139">AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="c3788-139">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="c3788-140">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="c3788-140">Set-AzureRmVMChefExtension</span></span>](./Set-AzureRmVMChefExtension.md)
