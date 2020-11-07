---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: 5a1d583d9eee535f519b6748867b4026dcc45006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625603"
---
# <span data-ttu-id="16ff3-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="16ff3-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="16ff3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="16ff3-102">SYNOPSIS</span></span>
<span data-ttu-id="16ff3-103">建立 Azure 可用性集。</span><span class="sxs-lookup"><span data-stu-id="16ff3-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16ff3-104">句法</span><span class="sxs-lookup"><span data-stu-id="16ff3-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16ff3-105">說明</span><span class="sxs-lookup"><span data-stu-id="16ff3-105">DESCRIPTION</span></span>
<span data-ttu-id="16ff3-106">**新的-AzureRmAvailabilitySet** Cmdlet 會建立 Azure 可用性集。</span><span class="sxs-lookup"><span data-stu-id="16ff3-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="16ff3-107">示例</span><span class="sxs-lookup"><span data-stu-id="16ff3-107">EXAMPLES</span></span>

### <span data-ttu-id="16ff3-108">範例1：建立可用性集</span><span class="sxs-lookup"><span data-stu-id="16ff3-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="16ff3-109">這個命令會在名為 [ResourceGroup11] 的資源群組中建立名為 AvailablitySet03 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="16ff3-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="16ff3-110">參數</span><span class="sxs-lookup"><span data-stu-id="16ff3-110">PARAMETERS</span></span>

### <span data-ttu-id="16ff3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16ff3-111">-AsJob</span></span>
<span data-ttu-id="16ff3-112">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="16ff3-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="16ff3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16ff3-113">-DefaultProfile</span></span>
<span data-ttu-id="16ff3-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="16ff3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16ff3-115">-位置</span><span class="sxs-lookup"><span data-stu-id="16ff3-115">-Location</span></span>
<span data-ttu-id="16ff3-116">指定可用性集的位置。</span><span class="sxs-lookup"><span data-stu-id="16ff3-116">Specifies the location for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16ff3-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="16ff3-117">-Name</span></span>
<span data-ttu-id="16ff3-118">指定可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="16ff3-118">Specifies a name for the availability set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16ff3-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="16ff3-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="16ff3-120">指定平臺容錯網域計數。</span><span class="sxs-lookup"><span data-stu-id="16ff3-120">Specifies the platform fault domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16ff3-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="16ff3-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="16ff3-122">指定平臺更新網域計數。</span><span class="sxs-lookup"><span data-stu-id="16ff3-122">Specifies the platform update domain count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16ff3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16ff3-123">-ResourceGroupName</span></span>
<span data-ttu-id="16ff3-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="16ff3-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="16ff3-125">-Sku</span><span class="sxs-lookup"><span data-stu-id="16ff3-125">-Sku</span></span>
<span data-ttu-id="16ff3-126">Sku 的名稱。</span><span class="sxs-lookup"><span data-stu-id="16ff3-126">The Name of Sku.</span></span>
<span data-ttu-id="16ff3-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="16ff3-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="16ff3-128">已對齊：適用于受管理的磁片</span><span class="sxs-lookup"><span data-stu-id="16ff3-128">Aligned: For managed disks</span></span>
- <span data-ttu-id="16ff3-129">傳統：適用于非託管磁片</span><span class="sxs-lookup"><span data-stu-id="16ff3-129">Classic: For unmanaged disks</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16ff3-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="16ff3-130">-Tag</span></span>
<span data-ttu-id="16ff3-131">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="16ff3-131">Key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16ff3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16ff3-132">CommonParameters</span></span>
<span data-ttu-id="16ff3-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="16ff3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16ff3-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="16ff3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16ff3-135">輸入</span><span class="sxs-lookup"><span data-stu-id="16ff3-135">INPUTS</span></span>

### <span data-ttu-id="16ff3-136">System.object</span><span class="sxs-lookup"><span data-stu-id="16ff3-136">System.String</span></span>

### <span data-ttu-id="16ff3-137">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="16ff3-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="16ff3-138">輸出</span><span class="sxs-lookup"><span data-stu-id="16ff3-138">OUTPUTS</span></span>

### <span data-ttu-id="16ff3-139">PSAvailabilitySet 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="16ff3-139">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="16ff3-140">筆記</span><span class="sxs-lookup"><span data-stu-id="16ff3-140">NOTES</span></span>

## <span data-ttu-id="16ff3-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="16ff3-141">RELATED LINKS</span></span>

[<span data-ttu-id="16ff3-142">AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="16ff3-142">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="16ff3-143">移除-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="16ff3-143">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


