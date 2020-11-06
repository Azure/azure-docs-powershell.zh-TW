---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: b5e9828c0cf9f73f88a44b7a4471a22bbfbe49af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448756"
---
# <span data-ttu-id="e0d4c-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e0d4c-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="e0d4c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e0d4c-102">SYNOPSIS</span></span>
<span data-ttu-id="e0d4c-103">建立 Azure 可用性集。</span><span class="sxs-lookup"><span data-stu-id="e0d4c-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0d4c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e0d4c-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [<CommonParameters>]
```

## <span data-ttu-id="e0d4c-105">說明</span><span class="sxs-lookup"><span data-stu-id="e0d4c-105">DESCRIPTION</span></span>
<span data-ttu-id="e0d4c-106">**新的-AzureRmAvailabilitySet** Cmdlet 會建立 Azure 可用性集。</span><span class="sxs-lookup"><span data-stu-id="e0d4c-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="e0d4c-107">示例</span><span class="sxs-lookup"><span data-stu-id="e0d4c-107">EXAMPLES</span></span>

### <span data-ttu-id="e0d4c-108">範例1：建立可用性集</span><span class="sxs-lookup"><span data-stu-id="e0d4c-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="e0d4c-109">這個命令會在名為 [ResourceGroup11] 的資源群組中建立名為 AvailablitySet03 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="e0d4c-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="e0d4c-110">參數</span><span class="sxs-lookup"><span data-stu-id="e0d4c-110">PARAMETERS</span></span>

### <span data-ttu-id="e0d4c-111">-位置</span><span class="sxs-lookup"><span data-stu-id="e0d4c-111">-Location</span></span>
<span data-ttu-id="e0d4c-112">指定可用性集的位置。</span><span class="sxs-lookup"><span data-stu-id="e0d4c-112">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="e0d4c-113">-管理</span><span class="sxs-lookup"><span data-stu-id="e0d4c-113">-Managed</span></span>
<span data-ttu-id="e0d4c-114">受管理的可用性集</span><span class="sxs-lookup"><span data-stu-id="e0d4c-114">Managed Availability Set</span></span>
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

### <span data-ttu-id="e0d4c-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="e0d4c-115">-Name</span></span>
<span data-ttu-id="e0d4c-116">指定可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0d4c-116">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="e0d4c-117">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="e0d4c-117">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="e0d4c-118">指定平臺容錯網域計數。</span><span class="sxs-lookup"><span data-stu-id="e0d4c-118">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="e0d4c-119">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="e0d4c-119">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="e0d4c-120">指定平臺更新網域計數。</span><span class="sxs-lookup"><span data-stu-id="e0d4c-120">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="e0d4c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0d4c-121">-ResourceGroupName</span></span>
<span data-ttu-id="e0d4c-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e0d4c-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="e0d4c-123">-Sku</span><span class="sxs-lookup"><span data-stu-id="e0d4c-123">-Sku</span></span>
<span data-ttu-id="e0d4c-124">Sku 的名稱</span><span class="sxs-lookup"><span data-stu-id="e0d4c-124">The Name of Sku</span></span>
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

### <span data-ttu-id="e0d4c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0d4c-125">CommonParameters</span></span>
<span data-ttu-id="e0d4c-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e0d4c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0d4c-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e0d4c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0d4c-128">輸入</span><span class="sxs-lookup"><span data-stu-id="e0d4c-128">INPUTS</span></span>

### <span data-ttu-id="e0d4c-129">所有</span><span class="sxs-lookup"><span data-stu-id="e0d4c-129">None</span></span>
<span data-ttu-id="e0d4c-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e0d4c-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e0d4c-131">輸出</span><span class="sxs-lookup"><span data-stu-id="e0d4c-131">OUTPUTS</span></span>

## <span data-ttu-id="e0d4c-132">筆記</span><span class="sxs-lookup"><span data-stu-id="e0d4c-132">NOTES</span></span>

## <span data-ttu-id="e0d4c-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="e0d4c-133">RELATED LINKS</span></span>

[<span data-ttu-id="e0d4c-134">AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e0d4c-134">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="e0d4c-135">移除-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="e0d4c-135">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


