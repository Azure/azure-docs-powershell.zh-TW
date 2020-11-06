---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: 32d3d5a152f36c0e4e5f8e3e4e4ecc2b8eb6ee31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449398"
---
# <span data-ttu-id="9347c-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9347c-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="9347c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9347c-102">SYNOPSIS</span></span>
<span data-ttu-id="9347c-103">取得虛擬機器上的診斷延伸設定。</span><span class="sxs-lookup"><span data-stu-id="9347c-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9347c-104">句法</span><span class="sxs-lookup"><span data-stu-id="9347c-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="9347c-105">說明</span><span class="sxs-lookup"><span data-stu-id="9347c-105">DESCRIPTION</span></span>
<span data-ttu-id="9347c-106">**AzureRmVMDiagnosticsExtension** Cmdlet 會取得虛擬機器上 Azure Diagnostics 延伸的設定。</span><span class="sxs-lookup"><span data-stu-id="9347c-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="9347c-107">示例</span><span class="sxs-lookup"><span data-stu-id="9347c-107">EXAMPLES</span></span>

### <span data-ttu-id="9347c-108">範例1：取得套用至虛擬機器的診斷延伸</span><span class="sxs-lookup"><span data-stu-id="9347c-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="9347c-109">這個命令會取得已套用到名為 ContosoVM22 的虛擬機器的診斷延伸。</span><span class="sxs-lookup"><span data-stu-id="9347c-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="9347c-110">參數</span><span class="sxs-lookup"><span data-stu-id="9347c-110">PARAMETERS</span></span>

### <span data-ttu-id="9347c-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="9347c-111">-Name</span></span>
<span data-ttu-id="9347c-112">指定此 Cmdlet 取得其設定的診斷延伸名稱。</span><span class="sxs-lookup"><span data-stu-id="9347c-112">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="9347c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9347c-113">-ResourceGroupName</span></span>
<span data-ttu-id="9347c-114">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9347c-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9347c-115">-狀態</span><span class="sxs-lookup"><span data-stu-id="9347c-115">-Status</span></span>
<span data-ttu-id="9347c-116">指示此 Cmdlet 使用 Status 值。</span><span class="sxs-lookup"><span data-stu-id="9347c-116">Indicates that this cmdlet uses the Status value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9347c-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="9347c-117">-VMName</span></span>
<span data-ttu-id="9347c-118">指定此 Cmdlet 取得診斷延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="9347c-118">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="9347c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9347c-119">CommonParameters</span></span>
<span data-ttu-id="9347c-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9347c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9347c-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9347c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9347c-122">輸入</span><span class="sxs-lookup"><span data-stu-id="9347c-122">INPUTS</span></span>

### <span data-ttu-id="9347c-123">所有</span><span class="sxs-lookup"><span data-stu-id="9347c-123">None</span></span>
<span data-ttu-id="9347c-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="9347c-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9347c-125">輸出</span><span class="sxs-lookup"><span data-stu-id="9347c-125">OUTPUTS</span></span>

## <span data-ttu-id="9347c-126">筆記</span><span class="sxs-lookup"><span data-stu-id="9347c-126">NOTES</span></span>

## <span data-ttu-id="9347c-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="9347c-127">RELATED LINKS</span></span>

[<span data-ttu-id="9347c-128">移除-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9347c-128">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="9347c-129">Set-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="9347c-129">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


