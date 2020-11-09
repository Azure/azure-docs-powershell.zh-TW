---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivatednszonegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateDnsZoneGroup.md
ms.openlocfilehash: 1012bd4da163b992aec049643feb1e3fd8b4bf76
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94288252"
---
# <span data-ttu-id="0a77e-101">Remove-AzPrivateDnsZoneGroup</span><span class="sxs-lookup"><span data-stu-id="0a77e-101">Remove-AzPrivateDnsZoneGroup</span></span>

## <span data-ttu-id="0a77e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0a77e-102">SYNOPSIS</span></span>
<span data-ttu-id="0a77e-103">移除 [DNS 區域] 群組。</span><span class="sxs-lookup"><span data-stu-id="0a77e-103">Removes a DNS zone group.</span></span>

## <span data-ttu-id="0a77e-104">句法</span><span class="sxs-lookup"><span data-stu-id="0a77e-104">SYNTAX</span></span>

```
Remove-AzPrivateDnsZoneGroup -ResourceGroupName <String> -PrivateEndpointName <String> -Name <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a77e-105">說明</span><span class="sxs-lookup"><span data-stu-id="0a77e-105">DESCRIPTION</span></span>
<span data-ttu-id="0a77e-106">**AzPrivateDnsZoneGroup** Cmdlet 會移除 [DNS 區域] 群組。</span><span class="sxs-lookup"><span data-stu-id="0a77e-106">The **Remove-AzPrivateDnsZoneGroup** cmdlet removes a DNS zone group.</span></span> 

## <span data-ttu-id="0a77e-107">示例</span><span class="sxs-lookup"><span data-stu-id="0a77e-107">EXAMPLES</span></span>

### <span data-ttu-id="0a77e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="0a77e-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzPrivateDnsZoneGroup -ResourceGroupName "rg" -PrivateEndpointName "test-pr-endpoint" -name dnsgroup1 
```

<span data-ttu-id="0a77e-109">上述範例會從端點 test pr-端點移除名為 dnsgroup1 的 DNS 區域 grup。</span><span class="sxs-lookup"><span data-stu-id="0a77e-109">Above example removes a DNS zone grup named dnsgroup1 from endpoint test-pr-endpoint.</span></span>

## <span data-ttu-id="0a77e-110">參數</span><span class="sxs-lookup"><span data-stu-id="0a77e-110">PARAMETERS</span></span>

### <span data-ttu-id="0a77e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a77e-111">-AsJob</span></span>
<span data-ttu-id="0a77e-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0a77e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0a77e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a77e-113">-DefaultProfile</span></span>
<span data-ttu-id="0a77e-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0a77e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a77e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0a77e-115">-Force</span></span>
<span data-ttu-id="0a77e-116">如果您想要刪除資源，請不要要求確認</span><span class="sxs-lookup"><span data-stu-id="0a77e-116">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="0a77e-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="0a77e-117">-Name</span></span>
<span data-ttu-id="0a77e-118">專用 dns 區域群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a77e-118">The name of the private dns zone group.</span></span>

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

### <span data-ttu-id="0a77e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a77e-119">-PassThru</span></span>
<span data-ttu-id="0a77e-120">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="0a77e-120">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="0a77e-121">-PrivateEndpointName</span><span class="sxs-lookup"><span data-stu-id="0a77e-121">-PrivateEndpointName</span></span>
<span data-ttu-id="0a77e-122">私人端點的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a77e-122">The name of the private endpoint.</span></span>

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

### <span data-ttu-id="0a77e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a77e-123">-ResourceGroupName</span></span>
<span data-ttu-id="0a77e-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0a77e-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="0a77e-125">-確認</span><span class="sxs-lookup"><span data-stu-id="0a77e-125">-Confirm</span></span>
<span data-ttu-id="0a77e-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0a77e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a77e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a77e-127">-WhatIf</span></span>
<span data-ttu-id="0a77e-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0a77e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a77e-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0a77e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a77e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a77e-130">CommonParameters</span></span>
<span data-ttu-id="0a77e-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0a77e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a77e-132">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0a77e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a77e-133">輸入</span><span class="sxs-lookup"><span data-stu-id="0a77e-133">INPUTS</span></span>

### <span data-ttu-id="0a77e-134">System.object</span><span class="sxs-lookup"><span data-stu-id="0a77e-134">System.String</span></span>

## <span data-ttu-id="0a77e-135">輸出</span><span class="sxs-lookup"><span data-stu-id="0a77e-135">OUTPUTS</span></span>

### <span data-ttu-id="0a77e-136">System.object</span><span class="sxs-lookup"><span data-stu-id="0a77e-136">System.Boolean</span></span>

## <span data-ttu-id="0a77e-137">筆記</span><span class="sxs-lookup"><span data-stu-id="0a77e-137">NOTES</span></span>

## <span data-ttu-id="0a77e-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="0a77e-138">RELATED LINKS</span></span>
