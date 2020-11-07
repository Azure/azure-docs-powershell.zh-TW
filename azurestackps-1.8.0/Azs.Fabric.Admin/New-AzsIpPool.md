---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd353b28b095178e83f488f3fd05a54146610b01
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2020
ms.locfileid: "93793493"
---
# <span data-ttu-id="c1ef3-101">New-AzsIpPool</span><span class="sxs-lookup"><span data-stu-id="c1ef3-101">New-AzsIpPool</span></span>

## <span data-ttu-id="c1ef3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c1ef3-102">SYNOPSIS</span></span>
<span data-ttu-id="c1ef3-103">建立基礎結構 IP 池。</span><span class="sxs-lookup"><span data-stu-id="c1ef3-103">Create an infrastructure IP pool.</span></span> <span data-ttu-id="c1ef3-104">建立 IP 池之後，就無法刪除或修改它。</span><span class="sxs-lookup"><span data-stu-id="c1ef3-104">Once created an IP pool cannot be deleted or modified.</span></span>

## <span data-ttu-id="c1ef3-105">句法</span><span class="sxs-lookup"><span data-stu-id="c1ef3-105">SYNTAX</span></span>

```
New-AzsIpPool [[-Name] <String>] [[-AddressPrefix] <String>] [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-Location] <String>] [[-ResourceGroupName] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1ef3-106">說明</span><span class="sxs-lookup"><span data-stu-id="c1ef3-106">DESCRIPTION</span></span>
<span data-ttu-id="c1ef3-107">建立基礎結構 IP 池。</span><span class="sxs-lookup"><span data-stu-id="c1ef3-107">Create an infrastructure IP pool.</span></span>

## <span data-ttu-id="c1ef3-108">示例</span><span class="sxs-lookup"><span data-stu-id="c1ef3-108">EXAMPLES</span></span>

### <span data-ttu-id="c1ef3-109">範例1</span><span class="sxs-lookup"><span data-stu-id="c1ef3-109">EXAMPLE 1</span></span>
```
New-AzsIpPool -Name IpPool4 -StartIpAddress ***.***.***.*** -EndIpAddress ***.***.***.*** -AddressPrefix ***.***.***.***/24
```

<span data-ttu-id="c1ef3-110">建立新的 IP 池。</span><span class="sxs-lookup"><span data-stu-id="c1ef3-110">Create a new IP pool.</span></span>

## <span data-ttu-id="c1ef3-111">參數</span><span class="sxs-lookup"><span data-stu-id="c1ef3-111">PARAMETERS</span></span>

### <span data-ttu-id="c1ef3-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="c1ef3-112">-Name</span></span>
<span data-ttu-id="c1ef3-113">IP 池名稱。</span><span class="sxs-lookup"><span data-stu-id="c1ef3-113">IP pool name.</span></span>

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

### <span data-ttu-id="c1ef3-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c1ef3-114">-AddressPrefix</span></span>
<span data-ttu-id="c1ef3-115">位址首碼。</span><span class="sxs-lookup"><span data-stu-id="c1ef3-115">The address prefix.</span></span>

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

### <span data-ttu-id="c1ef3-116">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="c1ef3-116">-StartIpAddress</span></span>
<span data-ttu-id="c1ef3-117">起始 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c1ef3-117">The starting IP address.</span></span>

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

### <span data-ttu-id="c1ef3-118">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="c1ef3-118">-EndIpAddress</span></span>
<span data-ttu-id="c1ef3-119">結束 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="c1ef3-119">The ending IP address.</span></span>

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

### <span data-ttu-id="c1ef3-120">-位置</span><span class="sxs-lookup"><span data-stu-id="c1ef3-120">-Location</span></span>
<span data-ttu-id="c1ef3-121">資源所在的地區。</span><span class="sxs-lookup"><span data-stu-id="c1ef3-121">The region where the resource is located.</span></span>

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

### <span data-ttu-id="c1ef3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1ef3-122">-ResourceGroupName</span></span>
<span data-ttu-id="c1ef3-123">已註冊資源提供者的資源群組。</span><span class="sxs-lookup"><span data-stu-id="c1ef3-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c1ef3-124">-標記</span><span class="sxs-lookup"><span data-stu-id="c1ef3-124">-Tags</span></span>
<span data-ttu-id="c1ef3-125">索引鍵/值對清單。</span><span class="sxs-lookup"><span data-stu-id="c1ef3-125">List of key-value pairs.</span></span>

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

### <span data-ttu-id="c1ef3-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1ef3-126">-AsJob</span></span>
<span data-ttu-id="c1ef3-127">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="c1ef3-127">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c1ef3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1ef3-128">-WhatIf</span></span>
<span data-ttu-id="c1ef3-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c1ef3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1ef3-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c1ef3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1ef3-131">-確認</span><span class="sxs-lookup"><span data-stu-id="c1ef3-131">-Confirm</span></span>
<span data-ttu-id="c1ef3-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c1ef3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1ef3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1ef3-133">CommonParameters</span></span>
<span data-ttu-id="c1ef3-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c1ef3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1ef3-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c1ef3-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1ef3-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c1ef3-136">INPUTS</span></span>

## <span data-ttu-id="c1ef3-137">輸出</span><span class="sxs-lookup"><span data-stu-id="c1ef3-137">OUTPUTS</span></span>

### <span data-ttu-id="c1ef3-138">ProvisioningState 中的 AzureStack （）</span><span class="sxs-lookup"><span data-stu-id="c1ef3-138">Microsoft.AzureStack.Management.Fabric.Admin.Models.ProvisioningState</span></span>

## <span data-ttu-id="c1ef3-139">筆記</span><span class="sxs-lookup"><span data-stu-id="c1ef3-139">NOTES</span></span>

## <span data-ttu-id="c1ef3-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1ef3-140">RELATED LINKS</span></span>
