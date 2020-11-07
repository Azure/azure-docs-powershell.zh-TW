---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbootdiagnostics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: e3e03083e831f38143423e69c84a67bfbc0440db
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795894"
---
# <span data-ttu-id="6f0f7-101">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="6f0f7-101">Set-AzVMBootDiagnostic</span></span>

## <span data-ttu-id="6f0f7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f0f7-102">SYNOPSIS</span></span>
<span data-ttu-id="6f0f7-103">修改虛擬機器的啟動診斷屬性。</span><span class="sxs-lookup"><span data-stu-id="6f0f7-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="6f0f7-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f0f7-104">SYNTAX</span></span>

### <span data-ttu-id="6f0f7-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="6f0f7-105">EnableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f0f7-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="6f0f7-106">DisableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f0f7-107">說明</span><span class="sxs-lookup"><span data-stu-id="6f0f7-107">DESCRIPTION</span></span>
<span data-ttu-id="6f0f7-108">**AzVMBootDiagnostic** Cmdlet 會修改虛擬機器的啟動診斷屬性。</span><span class="sxs-lookup"><span data-stu-id="6f0f7-108">The **Set-AzVMBootDiagnostic** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="6f0f7-109">示例</span><span class="sxs-lookup"><span data-stu-id="6f0f7-109">EXAMPLES</span></span>

### <span data-ttu-id="6f0f7-110">範例1：啟用啟動診斷程式</span><span class="sxs-lookup"><span data-stu-id="6f0f7-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="6f0f7-111">第一個命令會使用 **AzVM** 來取得名為 ContosoVM07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6f0f7-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="6f0f7-112">該命令會將它儲存在 $VM 變數中。</span><span class="sxs-lookup"><span data-stu-id="6f0f7-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="6f0f7-113">第二個命令會在 $VM 中啟用虛擬機器的引導診斷程式。</span><span class="sxs-lookup"><span data-stu-id="6f0f7-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="6f0f7-114">診斷資料會儲存在指定的帳號中。</span><span class="sxs-lookup"><span data-stu-id="6f0f7-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="6f0f7-115">參數</span><span class="sxs-lookup"><span data-stu-id="6f0f7-115">PARAMETERS</span></span>

### <span data-ttu-id="6f0f7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f0f7-116">-DefaultProfile</span></span>
<span data-ttu-id="6f0f7-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f0f7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f0f7-118">-停用</span><span class="sxs-lookup"><span data-stu-id="6f0f7-118">-Disable</span></span>
<span data-ttu-id="6f0f7-119">表示此 Cmdlet 會停用虛擬機器的啟動診斷程式。</span><span class="sxs-lookup"><span data-stu-id="6f0f7-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="6f0f7-120">-啟用</span><span class="sxs-lookup"><span data-stu-id="6f0f7-120">-Enable</span></span>
<span data-ttu-id="6f0f7-121">表示此 Cmdlet 會啟用虛擬機器的啟動診斷程式。</span><span class="sxs-lookup"><span data-stu-id="6f0f7-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

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

### <span data-ttu-id="6f0f7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f0f7-122">-ResourceGroupName</span></span>
<span data-ttu-id="6f0f7-123">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f0f7-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6f0f7-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6f0f7-124">-StorageAccountName</span></span>
<span data-ttu-id="6f0f7-125">指定儲存啟動診斷資料之儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="6f0f7-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

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

### <span data-ttu-id="6f0f7-126">-VM</span><span class="sxs-lookup"><span data-stu-id="6f0f7-126">-VM</span></span>
<span data-ttu-id="6f0f7-127">指定此 Cmdlet 變更其啟動診斷的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6f0f7-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="6f0f7-128">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f0f7-128">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="6f0f7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f0f7-129">CommonParameters</span></span>
<span data-ttu-id="6f0f7-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f0f7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f0f7-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6f0f7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f0f7-132">輸入</span><span class="sxs-lookup"><span data-stu-id="6f0f7-132">INPUTS</span></span>

### <span data-ttu-id="6f0f7-133">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6f0f7-133">PSVirtualMachine</span></span>
<span data-ttu-id="6f0f7-134">[VM "參數從管線接受類型 ' PSVirtualMachine」的值</span><span class="sxs-lookup"><span data-stu-id="6f0f7-134">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="6f0f7-135">輸出</span><span class="sxs-lookup"><span data-stu-id="6f0f7-135">OUTPUTS</span></span>

### <span data-ttu-id="6f0f7-136">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="6f0f7-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6f0f7-137">筆記</span><span class="sxs-lookup"><span data-stu-id="6f0f7-137">NOTES</span></span>

## <span data-ttu-id="6f0f7-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f0f7-138">RELATED LINKS</span></span>

[<span data-ttu-id="6f0f7-139">AzVM</span><span class="sxs-lookup"><span data-stu-id="6f0f7-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="6f0f7-140">AzVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="6f0f7-140">Get-AzVMBootDiagnosticsData</span></span>](./Get-AzVMBootDiagnosticsData.md)


