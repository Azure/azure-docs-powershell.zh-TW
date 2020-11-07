---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsssku
schema: 2.0.0
ms.openlocfilehash: 307b9852f506368e1e13c02fac4532dab4d2ddd2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801425"
---
# <span data-ttu-id="80ca9-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="80ca9-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="80ca9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="80ca9-102">SYNOPSIS</span></span>
<span data-ttu-id="80ca9-103">取得 VMSS 可用的 Sku。</span><span class="sxs-lookup"><span data-stu-id="80ca9-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="80ca9-104">句法</span><span class="sxs-lookup"><span data-stu-id="80ca9-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80ca9-105">說明</span><span class="sxs-lookup"><span data-stu-id="80ca9-105">DESCRIPTION</span></span>
<span data-ttu-id="80ca9-106">**AzureRmVmssSku** Cmdlet 會取得適用于虛擬機器規模集 (VMSS) 的可用 sku。</span><span class="sxs-lookup"><span data-stu-id="80ca9-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="80ca9-107">示例</span><span class="sxs-lookup"><span data-stu-id="80ca9-107">EXAMPLES</span></span>

### <span data-ttu-id="80ca9-108">範例1：從 VMSS 取得所有可用的 Sku</span><span class="sxs-lookup"><span data-stu-id="80ca9-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="80ca9-109">這個命令會從屬於名為 ContosoGroup 之資源群組的名為 ContosoVMSS 的 VMSS 中取得所有可用的 Sku。</span><span class="sxs-lookup"><span data-stu-id="80ca9-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="80ca9-110">參數</span><span class="sxs-lookup"><span data-stu-id="80ca9-110">PARAMETERS</span></span>

### <span data-ttu-id="80ca9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80ca9-111">-DefaultProfile</span></span>
<span data-ttu-id="80ca9-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="80ca9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80ca9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80ca9-113">-ResourceGroupName</span></span>
<span data-ttu-id="80ca9-114">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="80ca9-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="80ca9-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="80ca9-115">-VMScaleSetName</span></span>
<span data-ttu-id="80ca9-116">Species VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="80ca9-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="80ca9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80ca9-117">CommonParameters</span></span>
<span data-ttu-id="80ca9-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="80ca9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80ca9-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="80ca9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80ca9-120">輸入</span><span class="sxs-lookup"><span data-stu-id="80ca9-120">INPUTS</span></span>

### <span data-ttu-id="80ca9-121">所有</span><span class="sxs-lookup"><span data-stu-id="80ca9-121">None</span></span>
<span data-ttu-id="80ca9-122">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="80ca9-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="80ca9-123">輸出</span><span class="sxs-lookup"><span data-stu-id="80ca9-123">OUTPUTS</span></span>

### <span data-ttu-id="80ca9-124">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="80ca9-124">This cmdlet does not produce any output.</span></span>

## <span data-ttu-id="80ca9-125">筆記</span><span class="sxs-lookup"><span data-stu-id="80ca9-125">NOTES</span></span>

## <span data-ttu-id="80ca9-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="80ca9-126">RELATED LINKS</span></span>

[<span data-ttu-id="80ca9-127">AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="80ca9-127">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


