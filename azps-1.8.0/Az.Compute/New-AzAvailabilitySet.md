---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzAvailabilitySet.md
ms.openlocfilehash: c34bbb3cfd753c48a961373a44dd1e9bb4302208
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622768"
---
# <span data-ttu-id="592ac-101">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="592ac-101">New-AzAvailabilitySet</span></span>

## <span data-ttu-id="592ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="592ac-102">SYNOPSIS</span></span>
<span data-ttu-id="592ac-103">建立 Azure 可用性集。</span><span class="sxs-lookup"><span data-stu-id="592ac-103">Creates an Azure availability set.</span></span>

## <span data-ttu-id="592ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="592ac-104">SYNTAX</span></span>

```
New-AzAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="592ac-105">說明</span><span class="sxs-lookup"><span data-stu-id="592ac-105">DESCRIPTION</span></span>
<span data-ttu-id="592ac-106">**新的-AzAvailabilitySet** Cmdlet 會建立 Azure 可用性集。</span><span class="sxs-lookup"><span data-stu-id="592ac-106">The **New-AzAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="592ac-107">示例</span><span class="sxs-lookup"><span data-stu-id="592ac-107">EXAMPLES</span></span>

### <span data-ttu-id="592ac-108">範例1：建立可用性集</span><span class="sxs-lookup"><span data-stu-id="592ac-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="592ac-109">這個命令會在名為 [ResourceGroup11] 的資源群組中建立名為 AvailablitySet03 的可用性集。</span><span class="sxs-lookup"><span data-stu-id="592ac-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="592ac-110">參數</span><span class="sxs-lookup"><span data-stu-id="592ac-110">PARAMETERS</span></span>

### <span data-ttu-id="592ac-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="592ac-111">-AsJob</span></span>
<span data-ttu-id="592ac-112">在背景中執行 Cmdlet，然後返回作業來追蹤進度。</span><span class="sxs-lookup"><span data-stu-id="592ac-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="592ac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="592ac-113">-DefaultProfile</span></span>
<span data-ttu-id="592ac-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="592ac-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="592ac-115">-位置</span><span class="sxs-lookup"><span data-stu-id="592ac-115">-Location</span></span>
<span data-ttu-id="592ac-116">指定可用性集的位置。</span><span class="sxs-lookup"><span data-stu-id="592ac-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="592ac-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="592ac-117">-Name</span></span>
<span data-ttu-id="592ac-118">指定可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="592ac-118">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="592ac-119">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="592ac-119">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="592ac-120">指定平臺容錯網域計數。</span><span class="sxs-lookup"><span data-stu-id="592ac-120">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="592ac-121">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="592ac-121">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="592ac-122">指定平臺更新網域計數。</span><span class="sxs-lookup"><span data-stu-id="592ac-122">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="592ac-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="592ac-123">-ResourceGroupName</span></span>
<span data-ttu-id="592ac-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="592ac-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="592ac-125">-Sku</span><span class="sxs-lookup"><span data-stu-id="592ac-125">-Sku</span></span>
<span data-ttu-id="592ac-126">Sku 的名稱。</span><span class="sxs-lookup"><span data-stu-id="592ac-126">The Name of Sku.</span></span>
<span data-ttu-id="592ac-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="592ac-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="592ac-128">已對齊：適用于受管理的磁片</span><span class="sxs-lookup"><span data-stu-id="592ac-128">Aligned: For managed disks</span></span>
- <span data-ttu-id="592ac-129">傳統：適用于非託管磁片</span><span class="sxs-lookup"><span data-stu-id="592ac-129">Classic: For unmanaged disks</span></span>

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

### <span data-ttu-id="592ac-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="592ac-130">-Tag</span></span>
<span data-ttu-id="592ac-131">雜湊資料表形式的索引鍵/值對。</span><span class="sxs-lookup"><span data-stu-id="592ac-131">Key-value pairs in the form of a hash table.</span></span>

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

### <span data-ttu-id="592ac-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="592ac-132">CommonParameters</span></span>
<span data-ttu-id="592ac-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="592ac-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="592ac-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="592ac-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="592ac-135">輸入</span><span class="sxs-lookup"><span data-stu-id="592ac-135">INPUTS</span></span>

### <span data-ttu-id="592ac-136">System.object</span><span class="sxs-lookup"><span data-stu-id="592ac-136">System.String</span></span>

### <span data-ttu-id="592ac-137">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="592ac-137">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="592ac-138">輸出</span><span class="sxs-lookup"><span data-stu-id="592ac-138">OUTPUTS</span></span>

### <span data-ttu-id="592ac-139">PSAvailabilitySet 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="592ac-139">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="592ac-140">筆記</span><span class="sxs-lookup"><span data-stu-id="592ac-140">NOTES</span></span>

## <span data-ttu-id="592ac-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="592ac-141">RELATED LINKS</span></span>

[<span data-ttu-id="592ac-142">AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="592ac-142">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="592ac-143">移除-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="592ac-143">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


