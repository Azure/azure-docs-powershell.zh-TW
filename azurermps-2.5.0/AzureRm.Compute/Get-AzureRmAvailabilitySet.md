---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: ef00a9e425f67fbfc1ce47746503b574d483598f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800190"
---
# <span data-ttu-id="49995-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="49995-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="49995-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49995-102">SYNOPSIS</span></span>
<span data-ttu-id="49995-103">取得資源群組中的 Azure 可用性集合。</span><span class="sxs-lookup"><span data-stu-id="49995-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49995-104">句法</span><span class="sxs-lookup"><span data-stu-id="49995-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49995-105">說明</span><span class="sxs-lookup"><span data-stu-id="49995-105">DESCRIPTION</span></span>
<span data-ttu-id="49995-106">**AzureRmAvailabilitySet** Cmdlet 可在資源群組中取得 Azure 可用性集。</span><span class="sxs-lookup"><span data-stu-id="49995-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="49995-107">您可以指定要取得的特定可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="49995-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="49995-108">示例</span><span class="sxs-lookup"><span data-stu-id="49995-108">EXAMPLES</span></span>

### <span data-ttu-id="49995-109">範例1：取得特定的可用性集</span><span class="sxs-lookup"><span data-stu-id="49995-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="49995-110">這個命令會在名為 ResourceGroup11 的資源群組中取得名為 AvailablitySet03 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="49995-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="49995-111">範例2：取得所有的可用性集</span><span class="sxs-lookup"><span data-stu-id="49995-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="49995-112">這個命令會在名為 ResourceGroup11 的資源群組中取得所有的可用性集。</span><span class="sxs-lookup"><span data-stu-id="49995-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="49995-113">參數</span><span class="sxs-lookup"><span data-stu-id="49995-113">PARAMETERS</span></span>

### <span data-ttu-id="49995-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49995-114">-DefaultProfile</span></span>
<span data-ttu-id="49995-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49995-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49995-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="49995-116">-Name</span></span>
<span data-ttu-id="49995-117">指定此 Cmdlet 所取得之可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="49995-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49995-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49995-118">-ResourceGroupName</span></span>
<span data-ttu-id="49995-119">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="49995-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="49995-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49995-120">CommonParameters</span></span>
<span data-ttu-id="49995-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49995-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49995-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49995-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49995-123">輸入</span><span class="sxs-lookup"><span data-stu-id="49995-123">INPUTS</span></span>

### <span data-ttu-id="49995-124">所有</span><span class="sxs-lookup"><span data-stu-id="49995-124">None</span></span>
<span data-ttu-id="49995-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="49995-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="49995-126">輸出</span><span class="sxs-lookup"><span data-stu-id="49995-126">OUTPUTS</span></span>

### <span data-ttu-id="49995-127">PSAvailabilitySet 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="49995-127">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="49995-128">筆記</span><span class="sxs-lookup"><span data-stu-id="49995-128">NOTES</span></span>

## <span data-ttu-id="49995-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="49995-129">RELATED LINKS</span></span>

[<span data-ttu-id="49995-130">新-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="49995-130">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="49995-131">移除-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="49995-131">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


