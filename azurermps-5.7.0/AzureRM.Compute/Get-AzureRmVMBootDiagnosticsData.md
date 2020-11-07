---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 15CAC050-F2E9-4872-88E7-516A6D194FAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMBootDiagnosticsData.md
ms.openlocfilehash: 5ae237c21c78f206188f23153bdf35c6bea10b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623832"
---
# <span data-ttu-id="5dba2-101">Get-AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="5dba2-101">Get-AzureRmVMBootDiagnosticsData</span></span>

## <span data-ttu-id="5dba2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5dba2-102">SYNOPSIS</span></span>
<span data-ttu-id="5dba2-103">取得虛擬機器的啟動診斷資料。</span><span class="sxs-lookup"><span data-stu-id="5dba2-103">Gets boot diagnostics data for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dba2-104">句法</span><span class="sxs-lookup"><span data-stu-id="5dba2-104">SYNTAX</span></span>

### <span data-ttu-id="5dba2-105">WindowsParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5dba2-105">WindowsParamSet (Default)</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Windows]
 [-LocalPath] <String> [<CommonParameters>]
```

### <span data-ttu-id="5dba2-106">LinuxParamSet</span><span class="sxs-lookup"><span data-stu-id="5dba2-106">LinuxParamSet</span></span>
```
Get-AzureRmVMBootDiagnosticsData [-ResourceGroupName] <String> [-Name] <String> [-Linux]
 [[-LocalPath] <String>] [<CommonParameters>]
```

## <span data-ttu-id="5dba2-107">說明</span><span class="sxs-lookup"><span data-stu-id="5dba2-107">DESCRIPTION</span></span>
<span data-ttu-id="5dba2-108">**AzureRmVMBootDiagnosticsData** Cmdlet 會取得虛擬機器的啟動診斷資料。</span><span class="sxs-lookup"><span data-stu-id="5dba2-108">The **Get-AzureRmVMBootDiagnosticsData** cmdlet gets boot diagnostics data for a virtual machine.</span></span>

## <span data-ttu-id="5dba2-109">示例</span><span class="sxs-lookup"><span data-stu-id="5dba2-109">EXAMPLES</span></span>

### <span data-ttu-id="5dba2-110">範例1：取得啟動診斷資料</span><span class="sxs-lookup"><span data-stu-id="5dba2-110">Example 1: Get boot diagnostics data</span></span>
```
PS C:\> Get-AzureRmVMBootDiagnosticsData -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07" -Windows -LocalPath "C:\Contoso\BootDiagnostics"
```

<span data-ttu-id="5dba2-111">這個命令會取得名為 ContosoVM07 的虛擬機器的啟動診斷資料。</span><span class="sxs-lookup"><span data-stu-id="5dba2-111">This command gets boot diagnostics data for the virtual machine named ContosoVM07.</span></span>
<span data-ttu-id="5dba2-112">此虛擬機器會執行 Windows 作業系統。</span><span class="sxs-lookup"><span data-stu-id="5dba2-112">This virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="5dba2-113">該命令會將資料儲存在指定的本機路徑中。</span><span class="sxs-lookup"><span data-stu-id="5dba2-113">The command stores the data in specified local path.</span></span>

## <span data-ttu-id="5dba2-114">參數</span><span class="sxs-lookup"><span data-stu-id="5dba2-114">PARAMETERS</span></span>

### <span data-ttu-id="5dba2-115">-Linux</span><span class="sxs-lookup"><span data-stu-id="5dba2-115">-Linux</span></span>
<span data-ttu-id="5dba2-116">表示虛擬機器執行的是 Linux 作業系統。</span><span class="sxs-lookup"><span data-stu-id="5dba2-116">Indicates that the virtual machine runs the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dba2-117">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="5dba2-117">-LocalPath</span></span>
<span data-ttu-id="5dba2-118">指定啟動診斷資料的本機路徑。</span><span class="sxs-lookup"><span data-stu-id="5dba2-118">Specifies the local path for the boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: LinuxParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dba2-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="5dba2-119">-Name</span></span>
<span data-ttu-id="5dba2-120">指定此 Cmdlet 取得診斷資料之虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="5dba2-120">Specifies the name of the virtual machine for which this cmdlet gets diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dba2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dba2-121">-ResourceGroupName</span></span>
<span data-ttu-id="5dba2-122">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5dba2-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5dba2-123">-Windows</span><span class="sxs-lookup"><span data-stu-id="5dba2-123">-Windows</span></span>
<span data-ttu-id="5dba2-124">表示虛擬機器執行的是 Windows 作業系統。</span><span class="sxs-lookup"><span data-stu-id="5dba2-124">Indicates that the virtual machine runs the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dba2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dba2-125">CommonParameters</span></span>
<span data-ttu-id="5dba2-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5dba2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dba2-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5dba2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dba2-128">輸入</span><span class="sxs-lookup"><span data-stu-id="5dba2-128">INPUTS</span></span>

### <span data-ttu-id="5dba2-129">所有</span><span class="sxs-lookup"><span data-stu-id="5dba2-129">None</span></span>
<span data-ttu-id="5dba2-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="5dba2-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5dba2-131">輸出</span><span class="sxs-lookup"><span data-stu-id="5dba2-131">OUTPUTS</span></span>

## <span data-ttu-id="5dba2-132">筆記</span><span class="sxs-lookup"><span data-stu-id="5dba2-132">NOTES</span></span>

## <span data-ttu-id="5dba2-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="5dba2-133">RELATED LINKS</span></span>

[<span data-ttu-id="5dba2-134">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="5dba2-134">Set-AzureRmVMBootDiagnostics</span></span>](./Set-AzureRmVMBootDiagnostics.md)


