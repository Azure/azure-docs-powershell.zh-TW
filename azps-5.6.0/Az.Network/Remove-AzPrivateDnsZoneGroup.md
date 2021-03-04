---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: ada7faf13457f2c074a15b6e409e31afb93ac900
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912637"
---
# <span data-ttu-id="54a37-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="54a37-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="54a37-102">簡介</span><span class="sxs-lookup"><span data-stu-id="54a37-102">SYNOPSIS</span></span>
<span data-ttu-id="54a37-103">移除 DNS 區域群組。</span><span class="sxs-lookup"><span data-stu-id="54a37-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="54a37-104">語法</span><span class="sxs-lookup"><span data-stu-id="54a37-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54a37-105">描述</span><span class="sxs-lookup"><span data-stu-id="54a37-105">DESCRIPTION</span></span>
<span data-ttu-id="54a37-106">**Remove-AzPrivateDnsZoneGroup** Cmdlet 會移除 DNS 區域群組。</span><span class="sxs-lookup"><span data-stu-id="54a37-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="54a37-107">例子</span><span class="sxs-lookup"><span data-stu-id="54a37-107">EXAMPLES</span></span>

### <span data-ttu-id="54a37-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="54a37-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="54a37-109">上述範例會從端點 test-pr-endpoint 移除名為 dnsgroup1 的 DNS 區域 g下。</span><span class="sxs-lookup"><span data-stu-id="54a37-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="54a37-110">參數</span><span class="sxs-lookup"><span data-stu-id="54a37-110">PARAMETERS</span></span>

### <span data-ttu-id="54a37-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54a37-111">-AsJob</span></span>
<span data-ttu-id="54a37-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="54a37-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54a37-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54a37-113">-DefaultProfile</span></span>
<span data-ttu-id="54a37-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="54a37-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54a37-115">-強制</span><span class="sxs-lookup"><span data-stu-id="54a37-115">-Force</span></span>
<span data-ttu-id="54a37-116">如果您要刪除資源，請勿要求確認</span><span class="sxs-lookup"><span data-stu-id="54a37-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="54a37-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="54a37-117">-Name</span></span>
<span data-ttu-id="54a37-118">私人 dns 區域組的名稱。</span><span class="sxs-lookup"><span data-stu-id="54a37-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="54a37-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54a37-119">-PassThru</span></span>
<span data-ttu-id="54a37-120">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="54a37-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="54a37-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="54a37-121">-PrivateEndpointName</span></span>
<span data-ttu-id="54a37-122">私人端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="54a37-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="54a37-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54a37-123">-ResourceGroupName</span></span>
<span data-ttu-id="54a37-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="54a37-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="54a37-125">-確認</span><span class="sxs-lookup"><span data-stu-id="54a37-125">-Confirm</span></span>
<span data-ttu-id="54a37-126">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="54a37-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54a37-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54a37-127">-WhatIf</span></span>
<span data-ttu-id="54a37-128">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="54a37-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54a37-129">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54a37-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54a37-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54a37-130">CommonParameters</span></span>
<span data-ttu-id="54a37-131">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="54a37-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54a37-132">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54a37-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54a37-133">輸入</span><span class="sxs-lookup"><span data-stu-id="54a37-133">INPUTS</span></span>

### <span data-ttu-id="54a37-134">System.String</span><span class="sxs-lookup"><span data-stu-id="54a37-134">System.String</span></span>

## <span data-ttu-id="54a37-135">輸出</span><span class="sxs-lookup"><span data-stu-id="54a37-135">OUTPUTS</span></span>

### <span data-ttu-id="54a37-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="54a37-136">System.Boolean</span></span>

## <span data-ttu-id="54a37-137">筆記</span><span class="sxs-lookup"><span data-stu-id="54a37-137">NOTES</span></span>

## <span data-ttu-id="54a37-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="54a37-138">RELATED LINKS</span></span>
