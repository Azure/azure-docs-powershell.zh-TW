---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmAvailabilitySet.md
ms.openlocfilehash: 685dafeb72693a617ca627aa1abcae19c5e24389
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447454"
---
# <span data-ttu-id="09964-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="09964-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="09964-102">摘要</span><span class="sxs-lookup"><span data-stu-id="09964-102">SYNOPSIS</span></span>
<span data-ttu-id="09964-103">取得資源群組中的 Azure 可用性集合。</span><span class="sxs-lookup"><span data-stu-id="09964-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09964-104">句法</span><span class="sxs-lookup"><span data-stu-id="09964-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09964-105">說明</span><span class="sxs-lookup"><span data-stu-id="09964-105">DESCRIPTION</span></span>
<span data-ttu-id="09964-106">**AzureRmAvailabilitySet** Cmdlet 可在資源群組中取得 Azure 可用性集。</span><span class="sxs-lookup"><span data-stu-id="09964-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="09964-107">您可以指定要取得的特定可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="09964-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="09964-108">示例</span><span class="sxs-lookup"><span data-stu-id="09964-108">EXAMPLES</span></span>

### <span data-ttu-id="09964-109">範例1：取得特定的可用性集</span><span class="sxs-lookup"><span data-stu-id="09964-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="09964-110">這個命令會在名為 ResourceGroup11 的資源群組中取得名為 AvailablitySet03 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="09964-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="09964-111">範例2：取得所有的可用性集</span><span class="sxs-lookup"><span data-stu-id="09964-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="09964-112">這個命令會在名為 ResourceGroup11 的資源群組中取得所有的可用性集。</span><span class="sxs-lookup"><span data-stu-id="09964-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="09964-113">參數</span><span class="sxs-lookup"><span data-stu-id="09964-113">PARAMETERS</span></span>

### <span data-ttu-id="09964-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09964-114">-DefaultProfile</span></span>
<span data-ttu-id="09964-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="09964-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09964-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="09964-116">-Name</span></span>
<span data-ttu-id="09964-117">指定此 Cmdlet 所取得之可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="09964-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09964-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09964-118">-ResourceGroupName</span></span>
<span data-ttu-id="09964-119">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="09964-119">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09964-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09964-120">CommonParameters</span></span>
<span data-ttu-id="09964-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="09964-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09964-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="09964-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09964-123">輸入</span><span class="sxs-lookup"><span data-stu-id="09964-123">INPUTS</span></span>

### <span data-ttu-id="09964-124">System.object</span><span class="sxs-lookup"><span data-stu-id="09964-124">System.String</span></span>

## <span data-ttu-id="09964-125">輸出</span><span class="sxs-lookup"><span data-stu-id="09964-125">OUTPUTS</span></span>

### <span data-ttu-id="09964-126">PSAvailabilitySet 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="09964-126">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="09964-127">筆記</span><span class="sxs-lookup"><span data-stu-id="09964-127">NOTES</span></span>

## <span data-ttu-id="09964-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="09964-128">RELATED LINKS</span></span>

[<span data-ttu-id="09964-129">新-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="09964-129">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="09964-130">移除-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="09964-130">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


