---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b50cd7f98fd9919ed816314d7cec1222e5c4970c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93443387"
---
# <span data-ttu-id="152bd-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="152bd-101">New-AzsIpPool</span></span>

## <span data-ttu-id="152bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="152bd-102">SYNOPSIS</span></span>
<span data-ttu-id="152bd-103">建立基礎結構 IP 池。</span><span class="sxs-lookup"><span data-stu-id="152bd-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="152bd-104">建立 IP 池之後，就無法刪除或修改它。</span><span class="sxs-lookup"><span data-stu-id="152bd-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="152bd-105">句法</span><span class="sxs-lookup"><span data-stu-id="152bd-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="152bd-106">說明</span><span class="sxs-lookup"><span data-stu-id="152bd-106">DESCRIPTION</span></span>
<span data-ttu-id="152bd-107">建立基礎結構 IP 池。</span><span class="sxs-lookup"><span data-stu-id="152bd-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="152bd-108">示例</span><span class="sxs-lookup"><span data-stu-id="152bd-108">EXAMPLES</span></span>

### <span data-ttu-id="152bd-109">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="152bd-109">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="152bd-110">建立新的 IP 池。</span><span class="sxs-lookup"><span data-stu-id="152bd-110">Create a new IP pool.</span></span>

## <span data-ttu-id="152bd-111">參數</span><span class="sxs-lookup"><span data-stu-id="152bd-111">PARAMETERS</span></span>

### <span data-ttu-id="152bd-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="152bd-112">-AddressPrefix</span></span>
<span data-ttu-id="152bd-113">位址首碼。</span><span class="sxs-lookup"><span data-stu-id="152bd-113">The address prefix.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152bd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="152bd-114">-AsJob</span></span>
<span data-ttu-id="152bd-115">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="152bd-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152bd-116">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="152bd-116">-EndIpAddress</span></span>
<span data-ttu-id="152bd-117">結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="152bd-117">The ending IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152bd-118">-位置</span><span class="sxs-lookup"><span data-stu-id="152bd-118">-Location</span></span>
<span data-ttu-id="152bd-119">資源所在的地區。</span><span class="sxs-lookup"><span data-stu-id="152bd-119">The region where the resource is located.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152bd-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="152bd-120">-Name</span></span>
<span data-ttu-id="152bd-121">IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="152bd-121">IP pool name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152bd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="152bd-122">-ResourceGroupName</span></span>
<span data-ttu-id="152bd-123">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="152bd-123">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152bd-124">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="152bd-124">-StartIpAddress</span></span>
<span data-ttu-id="152bd-125">起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="152bd-125">The starting IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152bd-126">-標記</span><span class="sxs-lookup"><span data-stu-id="152bd-126">-Tags</span></span>
<span data-ttu-id="152bd-127">索引鍵/值對清單。</span><span class="sxs-lookup"><span data-stu-id="152bd-127">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152bd-128">-確認</span><span class="sxs-lookup"><span data-stu-id="152bd-128">-Confirm</span></span>
<span data-ttu-id="152bd-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="152bd-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152bd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="152bd-130">-WhatIf</span></span>
<span data-ttu-id="152bd-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="152bd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="152bd-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="152bd-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="152bd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="152bd-133">CommonParameters</span></span>
<span data-ttu-id="152bd-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="152bd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="152bd-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="152bd-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="152bd-136">輸入</span><span class="sxs-lookup"><span data-stu-id="152bd-136">INPUTS</span></span>

## <span data-ttu-id="152bd-137">輸出</span><span class="sxs-lookup"><span data-stu-id="152bd-137">OUTPUTS</span></span>

### <span data-ttu-id="152bd-138">ProvisioningState 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="152bd-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="152bd-139">筆記</span><span class="sxs-lookup"><span data-stu-id="152bd-139">NOTES</span></span>

## <span data-ttu-id="152bd-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="152bd-140">RELATED LINKS</span></span>

