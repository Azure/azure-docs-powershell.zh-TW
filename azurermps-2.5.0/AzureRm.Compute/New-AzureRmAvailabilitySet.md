---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: f08de8d1ea5f157270617c69a2092764d0ad4657
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800186"
---
# <span data-ttu-id="d8d06-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d8d06-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="d8d06-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d8d06-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d06-103">建立 Azure 可用性集。</span><span class="sxs-lookup"><span data-stu-id="d8d06-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8d06-104">句法</span><span class="sxs-lookup"><span data-stu-id="d8d06-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8d06-105">說明</span><span class="sxs-lookup"><span data-stu-id="d8d06-105">DESCRIPTION</span></span>
<span data-ttu-id="d8d06-106">**新的-AzureRmAvailabilitySet** Cmdlet 會建立 Azure 可用性集。</span><span class="sxs-lookup"><span data-stu-id="d8d06-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="d8d06-107">示例</span><span class="sxs-lookup"><span data-stu-id="d8d06-107">EXAMPLES</span></span>

### <span data-ttu-id="d8d06-108">範例1：建立可用性集</span><span class="sxs-lookup"><span data-stu-id="d8d06-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="d8d06-109">這個命令會在名為 [ResourceGroup11] 的資源群組中建立名為 AvailablitySet03 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="d8d06-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="d8d06-110">參數</span><span class="sxs-lookup"><span data-stu-id="d8d06-110">PARAMETERS</span></span>

### <span data-ttu-id="d8d06-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8d06-111">-AsJob</span></span>
<span data-ttu-id="d8d06-112">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="d8d06-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d06-113">-DefaultProfile</span></span>
<span data-ttu-id="d8d06-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d8d06-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8d06-115">-位置</span><span class="sxs-lookup"><span data-stu-id="d8d06-115">-Location</span></span>
<span data-ttu-id="d8d06-116">指定可用性集的位置。</span><span class="sxs-lookup"><span data-stu-id="d8d06-116">Specifies the location for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d06-117">-管理</span><span class="sxs-lookup"><span data-stu-id="d8d06-117">-Managed</span></span>
<span data-ttu-id="d8d06-118">受管理的可用性集</span><span class="sxs-lookup"><span data-stu-id="d8d06-118">Managed Availability Set</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d06-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="d8d06-119">-Name</span></span>
<span data-ttu-id="d8d06-120">指定可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8d06-120">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d06-121">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="d8d06-121">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="d8d06-122">指定平臺容錯網域計數。</span><span class="sxs-lookup"><span data-stu-id="d8d06-122">Specifies the platform fault domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d06-123">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="d8d06-123">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="d8d06-124">指定平臺更新網域計數。</span><span class="sxs-lookup"><span data-stu-id="d8d06-124">Specifies the platform update domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d06-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8d06-125">-ResourceGroupName</span></span>
<span data-ttu-id="d8d06-126">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d8d06-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d8d06-127">-Sku</span><span class="sxs-lookup"><span data-stu-id="d8d06-127">-Sku</span></span>
<span data-ttu-id="d8d06-128">Sku 的名稱</span><span class="sxs-lookup"><span data-stu-id="d8d06-128">The Name of Sku</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d06-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d06-129">CommonParameters</span></span>
<span data-ttu-id="d8d06-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d8d06-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d06-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d8d06-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d06-132">輸入</span><span class="sxs-lookup"><span data-stu-id="d8d06-132">INPUTS</span></span>

### <span data-ttu-id="d8d06-133">所有</span><span class="sxs-lookup"><span data-stu-id="d8d06-133">None</span></span>
<span data-ttu-id="d8d06-134">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d8d06-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d8d06-135">輸出</span><span class="sxs-lookup"><span data-stu-id="d8d06-135">OUTPUTS</span></span>

### <span data-ttu-id="d8d06-136">PSAvailabilitySet 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="d8d06-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="d8d06-137">筆記</span><span class="sxs-lookup"><span data-stu-id="d8d06-137">NOTES</span></span>

## <span data-ttu-id="d8d06-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="d8d06-138">RELATED LINKS</span></span>

[<span data-ttu-id="d8d06-139">AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d8d06-139">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="d8d06-140">移除-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d8d06-140">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


