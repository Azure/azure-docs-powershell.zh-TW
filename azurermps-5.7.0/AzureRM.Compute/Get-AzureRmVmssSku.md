---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
ms.openlocfilehash: c86bf549c0de3643aaba67143b7df78f6fce798c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446379"
---
# <span data-ttu-id="9cde3-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="9cde3-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="9cde3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9cde3-102">SYNOPSIS</span></span>
<span data-ttu-id="9cde3-103">取得 VMSS 可用的 Sku。</span><span class="sxs-lookup"><span data-stu-id="9cde3-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9cde3-104">句法</span><span class="sxs-lookup"><span data-stu-id="9cde3-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String> [<CommonParameters>]
```

## <span data-ttu-id="9cde3-105">說明</span><span class="sxs-lookup"><span data-stu-id="9cde3-105">DESCRIPTION</span></span>
<span data-ttu-id="9cde3-106">**AzureRmVmssSku** Cmdlet 會取得適用于虛擬機器規模集 (VMSS) 的可用 sku。</span><span class="sxs-lookup"><span data-stu-id="9cde3-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="9cde3-107">示例</span><span class="sxs-lookup"><span data-stu-id="9cde3-107">EXAMPLES</span></span>

### <span data-ttu-id="9cde3-108">範例1：從 VMSS 取得所有可用的 Sku</span><span class="sxs-lookup"><span data-stu-id="9cde3-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="9cde3-109">這個命令會從屬於名為 ContosoGroup 之資源群組的名為 ContosoVMSS 的 VMSS 中取得所有可用的 Sku。</span><span class="sxs-lookup"><span data-stu-id="9cde3-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="9cde3-110">參數</span><span class="sxs-lookup"><span data-stu-id="9cde3-110">PARAMETERS</span></span>

### <span data-ttu-id="9cde3-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cde3-111">-ResourceGroupName</span></span>
<span data-ttu-id="9cde3-112">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9cde3-112">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cde3-113">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9cde3-113">-VMScaleSetName</span></span>
<span data-ttu-id="9cde3-114">Species VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="9cde3-114">Species the name of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cde3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cde3-115">CommonParameters</span></span>
<span data-ttu-id="9cde3-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9cde3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cde3-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9cde3-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cde3-118">輸入</span><span class="sxs-lookup"><span data-stu-id="9cde3-118">INPUTS</span></span>

### <span data-ttu-id="9cde3-119">所有</span><span class="sxs-lookup"><span data-stu-id="9cde3-119">None</span></span>
<span data-ttu-id="9cde3-120">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="9cde3-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9cde3-121">輸出</span><span class="sxs-lookup"><span data-stu-id="9cde3-121">OUTPUTS</span></span>

### <span data-ttu-id="9cde3-122">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="9cde3-122">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="9cde3-123">筆記</span><span class="sxs-lookup"><span data-stu-id="9cde3-123">NOTES</span></span>

## <span data-ttu-id="9cde3-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="9cde3-124">RELATED LINKS</span></span>

[<span data-ttu-id="9cde3-125">AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9cde3-125">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


