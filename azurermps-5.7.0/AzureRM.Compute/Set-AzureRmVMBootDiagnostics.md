---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
ms.openlocfilehash: c02551e09fa0a5ce484883a4b2925c0c172e537f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447852"
---
# <span data-ttu-id="909b1-101">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="909b1-101">Set-AzureRmVMBootDiagnostics</span></span>

## <span data-ttu-id="909b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="909b1-102">SYNOPSIS</span></span>
<span data-ttu-id="909b1-103">修改虛擬機器的啟動診斷屬性。</span><span class="sxs-lookup"><span data-stu-id="909b1-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="909b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="909b1-104">SYNTAX</span></span>

### <span data-ttu-id="909b1-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="909b1-105">EnableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="909b1-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="909b1-106">DisableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [<CommonParameters>]
```

## <span data-ttu-id="909b1-107">說明</span><span class="sxs-lookup"><span data-stu-id="909b1-107">DESCRIPTION</span></span>
<span data-ttu-id="909b1-108">**AzureRmVMBootDiagnostics** Cmdlet 會修改虛擬機器的啟動診斷屬性。</span><span class="sxs-lookup"><span data-stu-id="909b1-108">The **Set-AzureRmVMBootDiagnostics** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="909b1-109">示例</span><span class="sxs-lookup"><span data-stu-id="909b1-109">EXAMPLES</span></span>

### <span data-ttu-id="909b1-110">範例1：啟用啟動診斷程式</span><span class="sxs-lookup"><span data-stu-id="909b1-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
PS C:\> Update-AzureRmVM -ResourceGroup "ResourceGroup11" -VM $VM
```

<span data-ttu-id="909b1-111">第一個命令會使用 **AzureRmVM** 來取得名為 ContosoVM07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="909b1-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="909b1-112">該命令會將它儲存在 $VM 變數中。</span><span class="sxs-lookup"><span data-stu-id="909b1-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="909b1-113">第二個命令會在 $VM 中啟用虛擬機器的引導診斷程式。</span><span class="sxs-lookup"><span data-stu-id="909b1-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="909b1-114">診斷資料會儲存在指定的帳號中。</span><span class="sxs-lookup"><span data-stu-id="909b1-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="909b1-115">參數</span><span class="sxs-lookup"><span data-stu-id="909b1-115">PARAMETERS</span></span>

### <span data-ttu-id="909b1-116">-停用</span><span class="sxs-lookup"><span data-stu-id="909b1-116">-Disable</span></span>
<span data-ttu-id="909b1-117">表示此 Cmdlet 會停用虛擬機器的啟動診斷程式。</span><span class="sxs-lookup"><span data-stu-id="909b1-117">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="909b1-118">-啟用</span><span class="sxs-lookup"><span data-stu-id="909b1-118">-Enable</span></span>
<span data-ttu-id="909b1-119">表示此 Cmdlet 會啟用虛擬機器的啟動診斷程式。</span><span class="sxs-lookup"><span data-stu-id="909b1-119">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="909b1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="909b1-120">-ResourceGroupName</span></span>
<span data-ttu-id="909b1-121">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="909b1-121">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="909b1-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="909b1-122">-StorageAccountName</span></span>
<span data-ttu-id="909b1-123">指定儲存啟動診斷資料之儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="909b1-123">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="909b1-124">-VM</span><span class="sxs-lookup"><span data-stu-id="909b1-124">-VM</span></span>
<span data-ttu-id="909b1-125">指定此 Cmdlet 變更其啟動診斷的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="909b1-125">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="909b1-126">若要取得虛擬機器物件，請使用 Get-AzureRmVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="909b1-126">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="909b1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="909b1-127">CommonParameters</span></span>
<span data-ttu-id="909b1-128">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="909b1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="909b1-129">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="909b1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="909b1-130">輸入</span><span class="sxs-lookup"><span data-stu-id="909b1-130">INPUTS</span></span>

### <span data-ttu-id="909b1-131">所有</span><span class="sxs-lookup"><span data-stu-id="909b1-131">None</span></span>
<span data-ttu-id="909b1-132">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="909b1-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="909b1-133">輸出</span><span class="sxs-lookup"><span data-stu-id="909b1-133">OUTPUTS</span></span>

## <span data-ttu-id="909b1-134">筆記</span><span class="sxs-lookup"><span data-stu-id="909b1-134">NOTES</span></span>

## <span data-ttu-id="909b1-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="909b1-135">RELATED LINKS</span></span>

[<span data-ttu-id="909b1-136">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="909b1-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="909b1-137">AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="909b1-137">Get-AzureRmVMBootDiagnosticsData</span></span>](./Get-AzureRmVMBootDiagnosticsData.md)


