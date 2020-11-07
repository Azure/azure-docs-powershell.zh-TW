---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbootdiagnostics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
ms.openlocfilehash: 290c726c53ea4479c4bd1f3cb9b2c607c04f20cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625336"
---
# <span data-ttu-id="90e89-101">Set-AzureRmVMBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="90e89-101">Set-AzureRmVMBootDiagnostics</span></span>

## <span data-ttu-id="90e89-102">摘要</span><span class="sxs-lookup"><span data-stu-id="90e89-102">SYNOPSIS</span></span>
<span data-ttu-id="90e89-103">修改虛擬機器的啟動診斷屬性。</span><span class="sxs-lookup"><span data-stu-id="90e89-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90e89-104">句法</span><span class="sxs-lookup"><span data-stu-id="90e89-104">SYNTAX</span></span>

### <span data-ttu-id="90e89-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="90e89-105">EnableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="90e89-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="90e89-106">DisableBootDiagnostics</span></span>
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90e89-107">說明</span><span class="sxs-lookup"><span data-stu-id="90e89-107">DESCRIPTION</span></span>
<span data-ttu-id="90e89-108">**AzureRmVMBootDiagnostics** Cmdlet 會修改虛擬機器的啟動診斷屬性。</span><span class="sxs-lookup"><span data-stu-id="90e89-108">The **Set-AzureRmVMBootDiagnostics** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="90e89-109">示例</span><span class="sxs-lookup"><span data-stu-id="90e89-109">EXAMPLES</span></span>

### <span data-ttu-id="90e89-110">範例1：啟用啟動診斷程式</span><span class="sxs-lookup"><span data-stu-id="90e89-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

<span data-ttu-id="90e89-111">第一個命令會使用 **AzureRmVM** 來取得名為 ContosoVM07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="90e89-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="90e89-112">該命令會將它儲存在 $VM 變數中。</span><span class="sxs-lookup"><span data-stu-id="90e89-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="90e89-113">第二個命令會在 $VM 中啟用虛擬機器的引導診斷程式。</span><span class="sxs-lookup"><span data-stu-id="90e89-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="90e89-114">診斷資料會儲存在指定的帳號中。</span><span class="sxs-lookup"><span data-stu-id="90e89-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="90e89-115">參數</span><span class="sxs-lookup"><span data-stu-id="90e89-115">PARAMETERS</span></span>

### <span data-ttu-id="90e89-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e89-116">-DefaultProfile</span></span>
<span data-ttu-id="90e89-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="90e89-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90e89-118">-停用</span><span class="sxs-lookup"><span data-stu-id="90e89-118">-Disable</span></span>
<span data-ttu-id="90e89-119">表示此 Cmdlet 會停用虛擬機器的啟動診斷程式。</span><span class="sxs-lookup"><span data-stu-id="90e89-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e89-120">-啟用</span><span class="sxs-lookup"><span data-stu-id="90e89-120">-Enable</span></span>
<span data-ttu-id="90e89-121">表示此 Cmdlet 會啟用虛擬機器的啟動診斷程式。</span><span class="sxs-lookup"><span data-stu-id="90e89-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e89-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90e89-122">-ResourceGroupName</span></span>
<span data-ttu-id="90e89-123">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="90e89-123">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e89-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="90e89-124">-StorageAccountName</span></span>
<span data-ttu-id="90e89-125">指定儲存啟動診斷資料之儲存空間帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="90e89-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90e89-126">-VM</span><span class="sxs-lookup"><span data-stu-id="90e89-126">-VM</span></span>
<span data-ttu-id="90e89-127">指定此 Cmdlet 變更其啟動診斷的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="90e89-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="90e89-128">若要取得虛擬機器物件，請使用 Get-AzureRmVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="90e89-128">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e89-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e89-129">CommonParameters</span></span>
<span data-ttu-id="90e89-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="90e89-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e89-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="90e89-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e89-132">輸入</span><span class="sxs-lookup"><span data-stu-id="90e89-132">INPUTS</span></span>

### <span data-ttu-id="90e89-133">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="90e89-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="90e89-134">System.object</span><span class="sxs-lookup"><span data-stu-id="90e89-134">System.String</span></span>

## <span data-ttu-id="90e89-135">輸出</span><span class="sxs-lookup"><span data-stu-id="90e89-135">OUTPUTS</span></span>

### <span data-ttu-id="90e89-136">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="90e89-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="90e89-137">筆記</span><span class="sxs-lookup"><span data-stu-id="90e89-137">NOTES</span></span>

## <span data-ttu-id="90e89-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="90e89-138">RELATED LINKS</span></span>

[<span data-ttu-id="90e89-139">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="90e89-139">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="90e89-140">AzureRmVMBootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="90e89-140">Get-AzureRmVMBootDiagnosticsData</span></span>](./Get-AzureRmVMBootDiagnosticsData.md)


