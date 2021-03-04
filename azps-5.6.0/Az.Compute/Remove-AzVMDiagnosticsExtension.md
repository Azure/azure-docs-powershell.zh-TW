---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 5b5a27be50da8a9c05b0cf766d48efe5844a0452
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916576"
---
# <span data-ttu-id="03c07-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="03c07-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="03c07-102">簡介</span><span class="sxs-lookup"><span data-stu-id="03c07-102">SYNOPSIS</span></span>
<span data-ttu-id="03c07-103">從虛擬機器移除診斷擴充功能。</span><span class="sxs-lookup"><span data-stu-id="03c07-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="03c07-104">語法</span><span class="sxs-lookup"><span data-stu-id="03c07-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03c07-105">描述</span><span class="sxs-lookup"><span data-stu-id="03c07-105">DESCRIPTION</span></span>
<span data-ttu-id="03c07-106">**Remove-Az VIRTUALDiagnosticsExtension** Cmdlet 會從虛擬機器移除 Azure 診斷擴充功能。</span><span class="sxs-lookup"><span data-stu-id="03c07-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="03c07-107">您必須將此 Cmdlet 的輸出傳遞至 Update-AzVM Cmdlet，以執行變更。</span><span class="sxs-lookup"><span data-stu-id="03c07-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="03c07-108">例子</span><span class="sxs-lookup"><span data-stu-id="03c07-108">EXAMPLES</span></span>

### <span data-ttu-id="03c07-109">範例 1：從虛擬機器移除診斷擴充功能</span><span class="sxs-lookup"><span data-stu-id="03c07-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="03c07-110">此命令會從名為 Contoso VIRTUAL22 的虛擬機器移除診斷擴充功能。</span><span class="sxs-lookup"><span data-stu-id="03c07-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="03c07-111">該命令會使用管線運算子Update-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="03c07-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="03c07-112">該命令會更新虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="03c07-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="03c07-113">參數</span><span class="sxs-lookup"><span data-stu-id="03c07-113">PARAMETERS</span></span>

### <span data-ttu-id="03c07-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03c07-114">-DefaultProfile</span></span>
<span data-ttu-id="03c07-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="03c07-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03c07-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="03c07-116">-Name</span></span>
<span data-ttu-id="03c07-117">指定此 Cmdlet 移除的診斷副檔名。</span><span class="sxs-lookup"><span data-stu-id="03c07-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="03c07-118">-NoWait</span><span class="sxs-lookup"><span data-stu-id="03c07-118">-NoWait</span></span>
<span data-ttu-id="03c07-119">啟動作業，並立即在作業完成之前返回。</span><span class="sxs-lookup"><span data-stu-id="03c07-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="03c07-120">若要判斷作業是否成功完成，請使用一些其他機制。</span><span class="sxs-lookup"><span data-stu-id="03c07-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="03c07-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03c07-121">-ResourceGroupName</span></span>
<span data-ttu-id="03c07-122">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="03c07-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="03c07-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="03c07-123">-VMName</span></span>
<span data-ttu-id="03c07-124">指定此 Cmdlet 會移除診斷副檔名的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="03c07-124">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="03c07-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03c07-125">CommonParameters</span></span>
<span data-ttu-id="03c07-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="03c07-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03c07-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03c07-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03c07-128">輸入</span><span class="sxs-lookup"><span data-stu-id="03c07-128">INPUTS</span></span>

### <span data-ttu-id="03c07-129">System.String</span><span class="sxs-lookup"><span data-stu-id="03c07-129">System.String</span></span>

## <span data-ttu-id="03c07-130">輸出</span><span class="sxs-lookup"><span data-stu-id="03c07-130">OUTPUTS</span></span>

### <span data-ttu-id="03c07-131">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="03c07-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="03c07-132">筆記</span><span class="sxs-lookup"><span data-stu-id="03c07-132">NOTES</span></span>

## <span data-ttu-id="03c07-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="03c07-133">RELATED LINKS</span></span>

[<span data-ttu-id="03c07-134">Get-AzMSDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="03c07-134">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="03c07-135">Set-AzMSDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="03c07-135">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="03c07-136">Update-AzMS</span><span class="sxs-lookup"><span data-stu-id="03c07-136">Update-AzVM</span></span>](./Update-AzVM.md)


