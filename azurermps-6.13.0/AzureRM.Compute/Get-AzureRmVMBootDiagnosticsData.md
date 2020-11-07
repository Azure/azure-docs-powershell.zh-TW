---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmbootdiagnosticsdata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
ms.openlocfilehash: 9d8da69f401f17aa757d5bb5e152f1557ee5356a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624909"
---
# <span data-ttu-id="7ae17-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="7ae17-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="7ae17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7ae17-102">SYNOPSIS</span></span>
<span data-ttu-id="7ae17-103">取得虛擬機器的啟動診斷資料。</span><span class="sxs-lookup"><span data-stu-id="7ae17-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ae17-104">句法</span><span class="sxs-lookup"><span data-stu-id="7ae17-104">SYNTAX</span></span>

### <span data-ttu-id="7ae17-105">WindowsParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7ae17-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ae17-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="7ae17-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ae17-107">說明</span><span class="sxs-lookup"><span data-stu-id="7ae17-107">DESCRIPTION</span></span>
<span data-ttu-id="7ae17-108">**AzureRmVMBootDiagnosticsData** Cmdlet 會取得虛擬機器的啟動診斷資料。</span><span class="sxs-lookup"><span data-stu-id="7ae17-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="7ae17-109">示例</span><span class="sxs-lookup"><span data-stu-id="7ae17-109">EXAMPLES</span></span>

### <span data-ttu-id="7ae17-110">範例1：取得啟動診斷資料</span><span class="sxs-lookup"><span data-stu-id="7ae17-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="7ae17-111">這個命令會取得名為 ContosoVM07 的虛擬機器的啟動診斷資料。</span><span class="sxs-lookup"><span data-stu-id="7ae17-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="7ae17-112">此虛擬機器會執行 Windows 作業系統。</span><span class="sxs-lookup"><span data-stu-id="7ae17-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="7ae17-113">該命令會將資料儲存在指定的本機路徑中。</span><span class="sxs-lookup"><span data-stu-id="7ae17-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="7ae17-114">參數</span><span class="sxs-lookup"><span data-stu-id="7ae17-114">PARAMETERS</span></span>

### <span data-ttu-id="7ae17-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ae17-115">-DefaultProfile</span></span>
<span data-ttu-id="7ae17-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7ae17-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ae17-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="7ae17-117">-Linux</span></span>
<span data-ttu-id="7ae17-118">表示虛擬機器執行的是 Linux 作業系統。</span><span class="sxs-lookup"><span data-stu-id="7ae17-118">Indicates that the virtual machine runs the Linux operating system.</span></span>

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

### <span data-ttu-id="7ae17-119">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="7ae17-119">-LocalPath</span></span>
<span data-ttu-id="7ae17-120">指定啟動診斷資料的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="7ae17-120">Specifies the local path for the boot diagnostics data.</span></span>

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

### <span data-ttu-id="7ae17-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="7ae17-121">-Name</span></span>
<span data-ttu-id="7ae17-122">指定此 Cmdlet 取得診斷資料之虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ae17-122">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

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

### <span data-ttu-id="7ae17-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ae17-123">-ResourceGroupName</span></span>
<span data-ttu-id="7ae17-124">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ae17-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7ae17-125">-Windows</span><span class="sxs-lookup"><span data-stu-id="7ae17-125">-Windows</span></span>
<span data-ttu-id="7ae17-126">表示虛擬機器執行的是 Windows 作業系統。</span><span class="sxs-lookup"><span data-stu-id="7ae17-126">Indicates that the virtual machine runs the Windows operating system.</span></span>

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

### <span data-ttu-id="7ae17-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ae17-127">CommonParameters</span></span>
<span data-ttu-id="7ae17-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7ae17-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ae17-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7ae17-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ae17-130">輸入</span><span class="sxs-lookup"><span data-stu-id="7ae17-130">INPUTS</span></span>

### <span data-ttu-id="7ae17-131">System.object</span><span class="sxs-lookup"><span data-stu-id="7ae17-131">System.String</span></span>

## <span data-ttu-id="7ae17-132">輸出</span><span class="sxs-lookup"><span data-stu-id="7ae17-132">OUTPUTS</span></span>

### <span data-ttu-id="7ae17-133">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="7ae17-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="7ae17-134">PSVirtualMachineInstanceView 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="7ae17-134">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="7ae17-135">筆記</span><span class="sxs-lookup"><span data-stu-id="7ae17-135">NOTES</span></span>

## <span data-ttu-id="7ae17-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ae17-136">RELATED LINKS</span></span>

[<span data-ttu-id="7ae17-137">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="7ae17-137">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)


