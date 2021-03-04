---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
ms.openlocfilehash: c0d672636d273bcd6e1d2c5f3ebc1c3b70a7b208
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917386"
---
# <span data-ttu-id="7fdf7-101">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="7fdf7-101">Get-AzVMChefExtension</span></span>

## <span data-ttu-id="7fdf7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7fdf7-102">SYNOPSIS</span></span>
<span data-ttu-id="7fdf7-103">進一步獲得有關擴充功能的資訊。</span><span class="sxs-lookup"><span data-stu-id="7fdf7-103">Gets information about a Chef extension.</span></span>

## <span data-ttu-id="7fdf7-104">語法</span><span class="sxs-lookup"><span data-stu-id="7fdf7-104">SYNTAX</span></span>

### <span data-ttu-id="7fdf7-105">Linux</span><span class="sxs-lookup"><span data-stu-id="7fdf7-105">Linux</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fdf7-106">窗戶</span><span class="sxs-lookup"><span data-stu-id="7fdf7-106">Windows</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fdf7-107">描述</span><span class="sxs-lookup"><span data-stu-id="7fdf7-107">DESCRIPTION</span></span>
<span data-ttu-id="7fdf7-108">**Get-Az VIRTUALChefExtension** Cmdlet 會取得安裝在虛擬機器上之一個總管擴充功能的資訊。</span><span class="sxs-lookup"><span data-stu-id="7fdf7-108">The **Get-AzVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="7fdf7-109">例子</span><span class="sxs-lookup"><span data-stu-id="7fdf7-109">EXAMPLES</span></span>

### <span data-ttu-id="7fdf7-110">範例 1：取得 Windows 虛擬機器的國元擴充功能詳細資料</span><span class="sxs-lookup"><span data-stu-id="7fdf7-110">Example 1: Get the details of Chef extension for a Windows virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="7fdf7-111">此命令會從名稱為 Windows MACHINE001 的 Windows 虛擬機器獲得一個名稱為 ResourceGroup001 的資源群組的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="7fdf7-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="7fdf7-112">範例 2：取得 Linux 虛擬機器的擴充功能詳細資料</span><span class="sxs-lookup"><span data-stu-id="7fdf7-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="7fdf7-113">此命令會從 Linux LINUX LINUX0001 的 Linux 虛擬機器獲得一個名稱為 ResourceGroup002 的資源群組的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="7fdf7-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="7fdf7-114">參數</span><span class="sxs-lookup"><span data-stu-id="7fdf7-114">PARAMETERS</span></span>

### <span data-ttu-id="7fdf7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fdf7-115">-DefaultProfile</span></span>
<span data-ttu-id="7fdf7-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7fdf7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fdf7-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="7fdf7-117">-Linux</span></span>
<span data-ttu-id="7fdf7-118">表示此 Cmdlet 適用于 Linux 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7fdf7-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

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

### <span data-ttu-id="7fdf7-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="7fdf7-119">-Name</span></span>
<span data-ttu-id="7fdf7-120">指定擴充功能的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fdf7-120">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="7fdf7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fdf7-121">-ResourceGroupName</span></span>
<span data-ttu-id="7fdf7-122">指定包含虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="7fdf7-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="7fdf7-123">-狀態</span><span class="sxs-lookup"><span data-stu-id="7fdf7-123">-Status</span></span>
<span data-ttu-id="7fdf7-124">表示此 Cmdlet 僅會獲得擴充名的 Instance view。</span><span class="sxs-lookup"><span data-stu-id="7fdf7-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fdf7-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="7fdf7-125">-VMName</span></span>
<span data-ttu-id="7fdf7-126">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fdf7-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="7fdf7-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="7fdf7-127">-Windows</span></span>
<span data-ttu-id="7fdf7-128">表示此 Cmdlet 適用于 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7fdf7-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

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

### <span data-ttu-id="7fdf7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fdf7-129">CommonParameters</span></span>
<span data-ttu-id="7fdf7-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7fdf7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fdf7-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fdf7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fdf7-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7fdf7-132">INPUTS</span></span>

### <span data-ttu-id="7fdf7-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7fdf7-133">System.String</span></span>

### <span data-ttu-id="7fdf7-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7fdf7-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7fdf7-135">輸出</span><span class="sxs-lookup"><span data-stu-id="7fdf7-135">OUTPUTS</span></span>

### <span data-ttu-id="7fdf7-136">Microsoft.Azure.Commands.Compute.models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="7fdf7-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="7fdf7-137">筆記</span><span class="sxs-lookup"><span data-stu-id="7fdf7-137">NOTES</span></span>

## <span data-ttu-id="7fdf7-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="7fdf7-138">RELATED LINKS</span></span>

[<span data-ttu-id="7fdf7-139">Set-AzEVChefExtension</span><span class="sxs-lookup"><span data-stu-id="7fdf7-139">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)

[<span data-ttu-id="7fdf7-140">Remove-AzEVChefExtension</span><span class="sxs-lookup"><span data-stu-id="7fdf7-140">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)


