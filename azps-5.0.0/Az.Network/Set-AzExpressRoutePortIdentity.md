---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: af04f3540aaf0ec90432c3b1262b45ef9ef1c2cd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286523"
---
# <span data-ttu-id="ffa31-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="ffa31-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="ffa31-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ffa31-102">SYNOPSIS</span></span>
<span data-ttu-id="ffa31-103">更新指派給 ExpressRoutePort 的身分識別。</span><span class="sxs-lookup"><span data-stu-id="ffa31-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="ffa31-104">句法</span><span class="sxs-lookup"><span data-stu-id="ffa31-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffa31-105">說明</span><span class="sxs-lookup"><span data-stu-id="ffa31-105">DESCRIPTION</span></span>
<span data-ttu-id="ffa31-106">**AzExpressRoutePortIdentity** Cmdlet 會更新本機 Azure ExpressRoutePort 物件。</span><span class="sxs-lookup"><span data-stu-id="ffa31-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="ffa31-107">使用 **AzExpressRoutePort** 將它指派給 ExpressRoutePort。</span><span class="sxs-lookup"><span data-stu-id="ffa31-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="ffa31-108">示例</span><span class="sxs-lookup"><span data-stu-id="ffa31-108">EXAMPLES</span></span>

### <span data-ttu-id="ffa31-109">範例1</span><span class="sxs-lookup"><span data-stu-id="ffa31-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="ffa31-110">參數</span><span class="sxs-lookup"><span data-stu-id="ffa31-110">PARAMETERS</span></span>

### <span data-ttu-id="ffa31-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffa31-111">-DefaultProfile</span></span>
<span data-ttu-id="ffa31-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ffa31-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffa31-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ffa31-113">-ExpressRoutePort</span></span>
<span data-ttu-id="ffa31-114">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="ffa31-114">The ExpressRoutePort</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa31-115">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="ffa31-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="ffa31-116">指派給 ExpressRoutePort 的使用者指派身分識別的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="ffa31-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffa31-117">-確認</span><span class="sxs-lookup"><span data-stu-id="ffa31-117">-Confirm</span></span>
<span data-ttu-id="ffa31-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ffa31-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffa31-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffa31-119">-WhatIf</span></span>
<span data-ttu-id="ffa31-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ffa31-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffa31-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ffa31-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffa31-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffa31-122">CommonParameters</span></span>
<span data-ttu-id="ffa31-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ffa31-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffa31-124">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ffa31-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffa31-125">輸入</span><span class="sxs-lookup"><span data-stu-id="ffa31-125">INPUTS</span></span>

### <span data-ttu-id="ffa31-126">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ffa31-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="ffa31-127">System.object</span><span class="sxs-lookup"><span data-stu-id="ffa31-127">System.String</span></span>

## <span data-ttu-id="ffa31-128">輸出</span><span class="sxs-lookup"><span data-stu-id="ffa31-128">OUTPUTS</span></span>

### <span data-ttu-id="ffa31-129">PSExpressRoutePort 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ffa31-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="ffa31-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ffa31-130">NOTES</span></span>

## <span data-ttu-id="ffa31-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ffa31-131">RELATED LINKS</span></span>
[<span data-ttu-id="ffa31-132">AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="ffa31-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="ffa31-133">新-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="ffa31-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="ffa31-134">移除-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="ffa31-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
