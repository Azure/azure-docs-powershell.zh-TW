---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 6b857356ea35476117a58f8f31f7174a7a91767a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613391"
---
# <span data-ttu-id="39ac9-101">Get-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="39ac9-101">Get-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="39ac9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="39ac9-103">取得虛擬機器上的診斷延伸設定。</span><span class="sxs-lookup"><span data-stu-id="39ac9-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="39ac9-104">句法</span><span class="sxs-lookup"><span data-stu-id="39ac9-104">SYNTAX</span></span>

```
Get-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39ac9-105">說明</span><span class="sxs-lookup"><span data-stu-id="39ac9-105">DESCRIPTION</span></span>
<span data-ttu-id="39ac9-106">**AzVMDiagnosticsExtension** Cmdlet 會取得虛擬機器上 Azure Diagnostics 延伸的設定。</span><span class="sxs-lookup"><span data-stu-id="39ac9-106">The **Get-AzVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="39ac9-107">示例</span><span class="sxs-lookup"><span data-stu-id="39ac9-107">EXAMPLES</span></span>

### <span data-ttu-id="39ac9-108">範例1：取得套用至虛擬機器的診斷延伸</span><span class="sxs-lookup"><span data-stu-id="39ac9-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="39ac9-109">這個命令會取得已套用到名為 ContosoVM22 的虛擬機器的診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="39ac9-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="39ac9-110">參數</span><span class="sxs-lookup"><span data-stu-id="39ac9-110">PARAMETERS</span></span>

### <span data-ttu-id="39ac9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39ac9-111">-DefaultProfile</span></span>
<span data-ttu-id="39ac9-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="39ac9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39ac9-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="39ac9-113">-Name</span></span>
<span data-ttu-id="39ac9-114">指定此 Cmdlet 取得其設定的診斷延伸名稱。</span><span class="sxs-lookup"><span data-stu-id="39ac9-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="39ac9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39ac9-115">-ResourceGroupName</span></span>
<span data-ttu-id="39ac9-116">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="39ac9-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="39ac9-117">-狀態</span><span class="sxs-lookup"><span data-stu-id="39ac9-117">-Status</span></span>
<span data-ttu-id="39ac9-118">指示此 Cmdlet 使用 Status 值。</span><span class="sxs-lookup"><span data-stu-id="39ac9-118">Indicates that this cmdlet uses the Status value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39ac9-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="39ac9-119">-VMName</span></span>
<span data-ttu-id="39ac9-120">指定此 Cmdlet 取得診斷延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="39ac9-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="39ac9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39ac9-121">CommonParameters</span></span>
<span data-ttu-id="39ac9-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39ac9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39ac9-123">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="39ac9-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39ac9-124">輸入</span><span class="sxs-lookup"><span data-stu-id="39ac9-124">INPUTS</span></span>

### <span data-ttu-id="39ac9-125">System.object</span><span class="sxs-lookup"><span data-stu-id="39ac9-125">System.String</span></span>

### <span data-ttu-id="39ac9-126">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="39ac9-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="39ac9-127">輸出</span><span class="sxs-lookup"><span data-stu-id="39ac9-127">OUTPUTS</span></span>

### <span data-ttu-id="39ac9-128">PSVirtualMachineExtension 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="39ac9-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="39ac9-129">筆記</span><span class="sxs-lookup"><span data-stu-id="39ac9-129">NOTES</span></span>

## <span data-ttu-id="39ac9-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="39ac9-130">RELATED LINKS</span></span>

[<span data-ttu-id="39ac9-131">移除-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="39ac9-131">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="39ac9-132">Set-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="39ac9-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)


