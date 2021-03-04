---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMBootDiagnosticsData.md
ms.openlocfilehash: 539e8b0a91c72d275f0997f2ebc69e86f4a9c901
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917389"
---
# <span data-ttu-id="e69f2-101">Get-AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="e69f2-101">Get-AzVMBootDiagnosticsData</span></span>

## <span data-ttu-id="e69f2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e69f2-102">SYNOPSIS</span></span>
<span data-ttu-id="e69f2-103">為虛擬機器獲得開機診斷資料。</span><span class="sxs-lookup"><span data-stu-id="e69f2-103">Gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="e69f2-104">語法</span><span class="sxs-lookup"><span data-stu-id="e69f2-104">SYNTAX</span></span>

### <span data-ttu-id="e69f2-105">WindowsParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e69f2-105">WindowsParamSet (Default)</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows] [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e69f2-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="e69f2-106">LinuxParamSet</span></span>
```
Get-AzVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux] [[-LocalPath] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e69f2-107">描述</span><span class="sxs-lookup"><span data-stu-id="e69f2-107">DESCRIPTION</span></span>
<span data-ttu-id="e69f2-108">**Get-Az VIRTUALBootDiagnosticsData** Cmdlet 會取得虛擬機器的開機診斷資料。</span><span class="sxs-lookup"><span data-stu-id="e69f2-108">The **Get-AzVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="e69f2-109">例子</span><span class="sxs-lookup"><span data-stu-id="e69f2-109">EXAMPLES</span></span>

### <span data-ttu-id="e69f2-110">範例 1：取得開機診斷資料</span><span class="sxs-lookup"><span data-stu-id="e69f2-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="e69f2-111">此命令會為名為 ContosoEV07 的虛擬機器獲得開機診斷資料。</span><span class="sxs-lookup"><span data-stu-id="e69f2-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="e69f2-112">此虛擬機器會執行 Windows 作業系統。</span><span class="sxs-lookup"><span data-stu-id="e69f2-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="e69f2-113">命令會以指定的本地路徑儲存資料。</span><span class="sxs-lookup"><span data-stu-id="e69f2-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="e69f2-114">參數</span><span class="sxs-lookup"><span data-stu-id="e69f2-114">PARAMETERS</span></span>

### <span data-ttu-id="e69f2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e69f2-115">-DefaultProfile</span></span>
<span data-ttu-id="e69f2-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e69f2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e69f2-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="e69f2-117">-Linux</span></span>
<span data-ttu-id="e69f2-118">表示虛擬機器執行 Linux 作業系統。</span><span class="sxs-lookup"><span data-stu-id="e69f2-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LinuxParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e69f2-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="e69f2-119">-LocalPath</span></span>
<span data-ttu-id="e69f2-120">指定開機診斷資料的本地路徑。</span><span class="sxs-lookup"><span data-stu-id="e69f2-120">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: LinuxParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e69f2-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e69f2-121">-Name</span></span>
<span data-ttu-id="e69f2-122">指定此 Cmdlet 會獲得診斷資料的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="e69f2-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e69f2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e69f2-123">-ResourceGroupName</span></span>
<span data-ttu-id="e69f2-124">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e69f2-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e69f2-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="e69f2-125">-Windows</span></span>
<span data-ttu-id="e69f2-126">表示虛擬機器執行 Windows 作業系統。</span><span class="sxs-lookup"><span data-stu-id="e69f2-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsParamSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e69f2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e69f2-127">CommonParameters</span></span>
<span data-ttu-id="e69f2-128">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e69f2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e69f2-129">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e69f2-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e69f2-130">輸入</span><span class="sxs-lookup"><span data-stu-id="e69f2-130">INPUTS</span></span>

### <span data-ttu-id="e69f2-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e69f2-131">System.String</span></span>

## <span data-ttu-id="e69f2-132">輸出</span><span class="sxs-lookup"><span data-stu-id="e69f2-132">OUTPUTS</span></span>

### <span data-ttu-id="e69f2-133">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="e69f2-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="e69f2-134">Microsoft.Azure.Commands.Compute.models.PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="e69f2-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="e69f2-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e69f2-135">NOTES</span></span>

## <span data-ttu-id="e69f2-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e69f2-136">RELATED LINKS</span></span>

[<span data-ttu-id="e69f2-137">Set-AzMSBOotDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e69f2-137">Set-AzVMBootDiagnostic</span></span>](./Set-AzVMBootDiagnostic.md)


