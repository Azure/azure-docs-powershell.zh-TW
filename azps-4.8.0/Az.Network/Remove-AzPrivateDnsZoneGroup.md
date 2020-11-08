---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 1012bd4da163b992aec049643feb1e3fd8b4bf76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126384"
---
# <span data-ttu-id="acf3f-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="acf3f-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="acf3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="acf3f-102">SYNOPSIS</span></span>
<span data-ttu-id="acf3f-103">移除 [DNS 區域] 群組。</span><span class="sxs-lookup"><span data-stu-id="acf3f-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="acf3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="acf3f-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acf3f-105">說明</span><span class="sxs-lookup"><span data-stu-id="acf3f-105">DESCRIPTION</span></span>
<span data-ttu-id="acf3f-106">**AzPrivateDnsZoneGroup** Cmdlet 會移除 [DNS 區域] 群組。</span><span class="sxs-lookup"><span data-stu-id="acf3f-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="acf3f-107">示例</span><span class="sxs-lookup"><span data-stu-id="acf3f-107">EXAMPLES</span></span>

### <span data-ttu-id="acf3f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="acf3f-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="acf3f-109">上述範例會從端點 test pr-端點移除名為 dnsgroup1 的 DNS 區域 grup。</span><span class="sxs-lookup"><span data-stu-id="acf3f-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="acf3f-110">參數</span><span class="sxs-lookup"><span data-stu-id="acf3f-110">PARAMETERS</span></span>

### <span data-ttu-id="acf3f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="acf3f-111">-AsJob</span></span>
<span data-ttu-id="acf3f-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="acf3f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="acf3f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf3f-113">-DefaultProfile</span></span>
<span data-ttu-id="acf3f-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="acf3f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acf3f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="acf3f-115">-Force</span></span>
<span data-ttu-id="acf3f-116">如果您想要刪除資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="acf3f-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="acf3f-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="acf3f-117">-Name</span></span>
<span data-ttu-id="acf3f-118">專用 dns 區域群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="acf3f-118">The name of the private dns zone group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PrivateDnsZoneGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf3f-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="acf3f-119">-PassThru</span></span>
<span data-ttu-id="acf3f-120">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="acf3f-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="acf3f-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="acf3f-121">-PrivateEndpointName</span></span>
<span data-ttu-id="acf3f-122">私人端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="acf3f-122">The name of the private endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf3f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acf3f-123">-ResourceGroupName</span></span>
<span data-ttu-id="acf3f-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="acf3f-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="acf3f-125">-確認</span><span class="sxs-lookup"><span data-stu-id="acf3f-125">-Confirm</span></span>
<span data-ttu-id="acf3f-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="acf3f-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf3f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acf3f-127">-WhatIf</span></span>
<span data-ttu-id="acf3f-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="acf3f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acf3f-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="acf3f-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf3f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf3f-130">CommonParameters</span></span>
<span data-ttu-id="acf3f-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="acf3f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf3f-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="acf3f-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf3f-133">輸入</span><span class="sxs-lookup"><span data-stu-id="acf3f-133">INPUTS</span></span>

### <span data-ttu-id="acf3f-134">System.object</span><span class="sxs-lookup"><span data-stu-id="acf3f-134">System.String</span></span>

## <span data-ttu-id="acf3f-135">輸出</span><span class="sxs-lookup"><span data-stu-id="acf3f-135">OUTPUTS</span></span>

### <span data-ttu-id="acf3f-136">System.object</span><span class="sxs-lookup"><span data-stu-id="acf3f-136">System.Boolean</span></span>

## <span data-ttu-id="acf3f-137">筆記</span><span class="sxs-lookup"><span data-stu-id="acf3f-137">NOTES</span></span>

## <span data-ttu-id="acf3f-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="acf3f-138">RELATED LINKS</span></span>
