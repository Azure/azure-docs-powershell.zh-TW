---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: 57e3aef7ff5b6acece0ccba1505d33f2add05ae2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801405"
---
# <span data-ttu-id="7522c-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7522c-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="7522c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7522c-102">SYNOPSIS</span></span>
<span data-ttu-id="7522c-103">從虛擬機器移除診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="7522c-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7522c-104">句法</span><span class="sxs-lookup"><span data-stu-id="7522c-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7522c-105">說明</span><span class="sxs-lookup"><span data-stu-id="7522c-105">DESCRIPTION</span></span>
<span data-ttu-id="7522c-106">**AzureRmVMDiagnosticsExtension** Cmdlet 會從虛擬機器中移除 Azure 診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="7522c-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="7522c-107">您必須將這個 Cmdlet 的輸出傳遞到 Update-AzureRmVM Cmdlet，才能實現您的變更。</span><span class="sxs-lookup"><span data-stu-id="7522c-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="7522c-108">示例</span><span class="sxs-lookup"><span data-stu-id="7522c-108">EXAMPLES</span></span>

### <span data-ttu-id="7522c-109">範例1：從虛擬機器移除診斷延伸</span><span class="sxs-lookup"><span data-stu-id="7522c-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="7522c-110">這個命令會從名為 ContosoVM22 的虛擬機器中移除診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="7522c-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="7522c-111">命令會使用管線運算子，將結果傳遞到 Update-AzureRmVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7522c-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7522c-112">該命令會更新虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7522c-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="7522c-113">參數</span><span class="sxs-lookup"><span data-stu-id="7522c-113">PARAMETERS</span></span>

### <span data-ttu-id="7522c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7522c-114">-DefaultProfile</span></span>
<span data-ttu-id="7522c-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7522c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7522c-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="7522c-116">-Name</span></span>
<span data-ttu-id="7522c-117">指定此 Cmdlet 移除的診斷延伸名稱。</span><span class="sxs-lookup"><span data-stu-id="7522c-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7522c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7522c-118">-ResourceGroupName</span></span>
<span data-ttu-id="7522c-119">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7522c-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7522c-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="7522c-120">-VMName</span></span>
<span data-ttu-id="7522c-121">指定此 Cmdlet 移除診斷延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="7522c-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="7522c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7522c-122">CommonParameters</span></span>
<span data-ttu-id="7522c-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7522c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7522c-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7522c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7522c-125">輸入</span><span class="sxs-lookup"><span data-stu-id="7522c-125">INPUTS</span></span>

### <span data-ttu-id="7522c-126">所有</span><span class="sxs-lookup"><span data-stu-id="7522c-126">None</span></span>
<span data-ttu-id="7522c-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="7522c-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7522c-128">輸出</span><span class="sxs-lookup"><span data-stu-id="7522c-128">OUTPUTS</span></span>

### <span data-ttu-id="7522c-129">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="7522c-129">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7522c-130">筆記</span><span class="sxs-lookup"><span data-stu-id="7522c-130">NOTES</span></span>

## <span data-ttu-id="7522c-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="7522c-131">RELATED LINKS</span></span>

[<span data-ttu-id="7522c-132">AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7522c-132">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="7522c-133">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7522c-133">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="7522c-134">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7522c-134">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

