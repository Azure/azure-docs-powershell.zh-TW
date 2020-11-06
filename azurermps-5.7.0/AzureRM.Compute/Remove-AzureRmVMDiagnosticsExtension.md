---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
ms.openlocfilehash: b9c2499c3172fcd34000c8adaa0bde144217bcbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448731"
---
# <span data-ttu-id="4e9dc-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="4e9dc-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="4e9dc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e9dc-102">SYNOPSIS</span></span>
<span data-ttu-id="4e9dc-103">從虛擬機器移除診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="4e9dc-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e9dc-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e9dc-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e9dc-105">說明</span><span class="sxs-lookup"><span data-stu-id="4e9dc-105">DESCRIPTION</span></span>
<span data-ttu-id="4e9dc-106">**AzureRmVMDiagnosticsExtension** Cmdlet 會從虛擬機器中移除 Azure 診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="4e9dc-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="4e9dc-107">您必須將這個 Cmdlet 的輸出傳遞到 Update-AzureRmVM Cmdlet，才能實現您的變更。</span><span class="sxs-lookup"><span data-stu-id="4e9dc-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="4e9dc-108">示例</span><span class="sxs-lookup"><span data-stu-id="4e9dc-108">EXAMPLES</span></span>

### <span data-ttu-id="4e9dc-109">範例1：從虛擬機器移除診斷延伸</span><span class="sxs-lookup"><span data-stu-id="4e9dc-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="4e9dc-110">這個命令會從名為 ContosoVM22 的虛擬機器中移除診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="4e9dc-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="4e9dc-111">命令會使用管線運算子，將結果傳遞到 Update-AzureRmVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e9dc-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="4e9dc-112">該命令會更新虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="4e9dc-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="4e9dc-113">參數</span><span class="sxs-lookup"><span data-stu-id="4e9dc-113">PARAMETERS</span></span>

### <span data-ttu-id="4e9dc-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e9dc-114">-Name</span></span>
<span data-ttu-id="4e9dc-115">指定此 Cmdlet 移除的診斷延伸名稱。</span><span class="sxs-lookup"><span data-stu-id="4e9dc-115">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4e9dc-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e9dc-116">-ResourceGroupName</span></span>
<span data-ttu-id="4e9dc-117">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e9dc-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="4e9dc-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="4e9dc-118">-VMName</span></span>
<span data-ttu-id="4e9dc-119">指定此 Cmdlet 移除診斷延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="4e9dc-119">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="4e9dc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e9dc-120">CommonParameters</span></span>
<span data-ttu-id="4e9dc-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e9dc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e9dc-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4e9dc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e9dc-123">輸入</span><span class="sxs-lookup"><span data-stu-id="4e9dc-123">INPUTS</span></span>

### <span data-ttu-id="4e9dc-124">所有</span><span class="sxs-lookup"><span data-stu-id="4e9dc-124">None</span></span>
<span data-ttu-id="4e9dc-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="4e9dc-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4e9dc-126">輸出</span><span class="sxs-lookup"><span data-stu-id="4e9dc-126">OUTPUTS</span></span>

## <span data-ttu-id="4e9dc-127">筆記</span><span class="sxs-lookup"><span data-stu-id="4e9dc-127">NOTES</span></span>

## <span data-ttu-id="4e9dc-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e9dc-128">RELATED LINKS</span></span>

[<span data-ttu-id="4e9dc-129">AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="4e9dc-129">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="4e9dc-130">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="4e9dc-130">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="4e9dc-131">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4e9dc-131">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


