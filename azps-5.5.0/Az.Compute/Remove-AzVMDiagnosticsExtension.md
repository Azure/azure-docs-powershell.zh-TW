---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 991b33bed897b0d33d9e5e0125dd7d9309f55bcd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127791"
---
# <span data-ttu-id="9acdc-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9acdc-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="9acdc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9acdc-102">SYNOPSIS</span></span>
<span data-ttu-id="9acdc-103">從虛擬機器移除診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="9acdc-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="9acdc-104">句法</span><span class="sxs-lookup"><span data-stu-id="9acdc-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9acdc-105">說明</span><span class="sxs-lookup"><span data-stu-id="9acdc-105">DESCRIPTION</span></span>
<span data-ttu-id="9acdc-106">**AzVMDiagnosticsExtension** Cmdlet 會從虛擬機器中移除 Azure 診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="9acdc-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="9acdc-107">您必須將這個 Cmdlet 的輸出傳遞到 Update-AzVM Cmdlet，才能實現您的變更。</span><span class="sxs-lookup"><span data-stu-id="9acdc-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="9acdc-108">示例</span><span class="sxs-lookup"><span data-stu-id="9acdc-108">EXAMPLES</span></span>

### <span data-ttu-id="9acdc-109">範例1：從虛擬機器移除診斷延伸</span><span class="sxs-lookup"><span data-stu-id="9acdc-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="9acdc-110">這個命令會從名為 ContosoVM22 的虛擬機器中移除診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="9acdc-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="9acdc-111">命令會使用管線運算子，將結果傳遞到 Update-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9acdc-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9acdc-112">該命令會更新虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="9acdc-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="9acdc-113">參數</span><span class="sxs-lookup"><span data-stu-id="9acdc-113">PARAMETERS</span></span>

### <span data-ttu-id="9acdc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9acdc-114">-DefaultProfile</span></span>
<span data-ttu-id="9acdc-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9acdc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9acdc-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="9acdc-116">-Name</span></span>
<span data-ttu-id="9acdc-117">指定此 Cmdlet 移除的診斷延伸名稱。</span><span class="sxs-lookup"><span data-stu-id="9acdc-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="9acdc-118">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9acdc-118">-NoWait</span></span>
<span data-ttu-id="9acdc-119">在作業完成之前，立即開始作業並立即返回。</span><span class="sxs-lookup"><span data-stu-id="9acdc-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="9acdc-120">若要判斷該作業是否已順利完成，請使用一些其他的機制。</span><span class="sxs-lookup"><span data-stu-id="9acdc-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9acdc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9acdc-121">-ResourceGroupName</span></span>
<span data-ttu-id="9acdc-122">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9acdc-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9acdc-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="9acdc-123">-VMName</span></span>
<span data-ttu-id="9acdc-124">指定此 Cmdlet 移除診斷延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="9acdc-124">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="9acdc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9acdc-125">CommonParameters</span></span>
<span data-ttu-id="9acdc-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9acdc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9acdc-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9acdc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9acdc-128">輸入</span><span class="sxs-lookup"><span data-stu-id="9acdc-128">INPUTS</span></span>

### <span data-ttu-id="9acdc-129">System.object</span><span class="sxs-lookup"><span data-stu-id="9acdc-129">System.String</span></span>

## <span data-ttu-id="9acdc-130">輸出</span><span class="sxs-lookup"><span data-stu-id="9acdc-130">OUTPUTS</span></span>

### <span data-ttu-id="9acdc-131">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="9acdc-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9acdc-132">筆記</span><span class="sxs-lookup"><span data-stu-id="9acdc-132">NOTES</span></span>

## <span data-ttu-id="9acdc-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="9acdc-133">RELATED LINKS</span></span>

[<span data-ttu-id="9acdc-134">AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9acdc-134">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="9acdc-135">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9acdc-135">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="9acdc-136">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="9acdc-136">Update-AzVM</span></span>](./Update-AzVM.md)


