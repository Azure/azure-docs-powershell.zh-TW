---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: bec83334032b3d0e18c017bc24d19d381a765176
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796029"
---
# <span data-ttu-id="61cb4-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="61cb4-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="61cb4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61cb4-102">SYNOPSIS</span></span>
<span data-ttu-id="61cb4-103">從虛擬機器移除診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="61cb4-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="61cb4-104">句法</span><span class="sxs-lookup"><span data-stu-id="61cb4-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61cb4-105">說明</span><span class="sxs-lookup"><span data-stu-id="61cb4-105">DESCRIPTION</span></span>
<span data-ttu-id="61cb4-106">**AzVMDiagnosticsExtension** Cmdlet 會從虛擬機器中移除 Azure 診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="61cb4-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="61cb4-107">您必須將這個 Cmdlet 的輸出傳遞到 Update-AzVM Cmdlet，才能實現您的變更。</span><span class="sxs-lookup"><span data-stu-id="61cb4-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="61cb4-108">示例</span><span class="sxs-lookup"><span data-stu-id="61cb4-108">EXAMPLES</span></span>

### <span data-ttu-id="61cb4-109">範例1：從虛擬機器移除診斷延伸</span><span class="sxs-lookup"><span data-stu-id="61cb4-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="61cb4-110">這個命令會從名為 ContosoVM22 的虛擬機器中移除診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="61cb4-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="61cb4-111">命令會使用管線運算子，將結果傳遞到 Update-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61cb4-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="61cb4-112">該命令會更新虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="61cb4-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="61cb4-113">參數</span><span class="sxs-lookup"><span data-stu-id="61cb4-113">PARAMETERS</span></span>

### <span data-ttu-id="61cb4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61cb4-114">-DefaultProfile</span></span>
<span data-ttu-id="61cb4-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="61cb4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61cb4-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="61cb4-116">-Name</span></span>
<span data-ttu-id="61cb4-117">指定此 Cmdlet 移除的診斷延伸名稱。</span><span class="sxs-lookup"><span data-stu-id="61cb4-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="61cb4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61cb4-118">-ResourceGroupName</span></span>
<span data-ttu-id="61cb4-119">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="61cb4-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="61cb4-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="61cb4-120">-VMName</span></span>
<span data-ttu-id="61cb4-121">指定此 Cmdlet 移除診斷延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="61cb4-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="61cb4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61cb4-122">CommonParameters</span></span>
<span data-ttu-id="61cb4-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61cb4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61cb4-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="61cb4-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61cb4-125">輸入</span><span class="sxs-lookup"><span data-stu-id="61cb4-125">INPUTS</span></span>

### <span data-ttu-id="61cb4-126">所有</span><span class="sxs-lookup"><span data-stu-id="61cb4-126">None</span></span>
<span data-ttu-id="61cb4-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="61cb4-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="61cb4-128">輸出</span><span class="sxs-lookup"><span data-stu-id="61cb4-128">OUTPUTS</span></span>

### <span data-ttu-id="61cb4-129">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="61cb4-129">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="61cb4-130">筆記</span><span class="sxs-lookup"><span data-stu-id="61cb4-130">NOTES</span></span>

## <span data-ttu-id="61cb4-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="61cb4-131">RELATED LINKS</span></span>

[<span data-ttu-id="61cb4-132">AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="61cb4-132">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="61cb4-133">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="61cb4-133">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="61cb4-134">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="61cb4-134">Update-AzVM</span></span>](./Update-AzVM.md)


