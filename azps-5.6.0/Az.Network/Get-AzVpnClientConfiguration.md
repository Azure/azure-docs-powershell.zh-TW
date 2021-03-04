---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: 03ed4fe9ad6e8b2e7c5af0b24e29c351a2b776f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916729"
---
# <span data-ttu-id="339ce-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="339ce-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="339ce-102">簡介</span><span class="sxs-lookup"><span data-stu-id="339ce-102">SYNOPSIS</span></span>
<span data-ttu-id="339ce-103">讓使用者輕鬆下載使用命令小命令產生的 vpn 設定檔套件New-AzVpnClientConfiguration套件。</span><span class="sxs-lookup"><span data-stu-id="339ce-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="339ce-104">語法</span><span class="sxs-lookup"><span data-stu-id="339ce-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="339ce-105">描述</span><span class="sxs-lookup"><span data-stu-id="339ce-105">DESCRIPTION</span></span>
<span data-ttu-id="339ce-106">此Get-AzVpnClientConfiguration會返回可從其中下載 VPN 用戶端的 URL。</span><span class="sxs-lookup"><span data-stu-id="339ce-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="339ce-107">例子</span><span class="sxs-lookup"><span data-stu-id="339ce-107">EXAMPLES</span></span>

### <span data-ttu-id="339ce-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="339ce-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="339ce-109">獲得 URL 以下載先前使用 New-AzVpnClientConfiguration 產生的 VpnClient 設定檔。</span><span class="sxs-lookup"><span data-stu-id="339ce-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="339ce-110">參數</span><span class="sxs-lookup"><span data-stu-id="339ce-110">PARAMETERS</span></span>

### <span data-ttu-id="339ce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="339ce-111">-DefaultProfile</span></span>
<span data-ttu-id="339ce-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="339ce-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="339ce-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="339ce-113">-Name</span></span>
<span data-ttu-id="339ce-114">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="339ce-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="339ce-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="339ce-115">-ResourceGroupName</span></span>
<span data-ttu-id="339ce-116">資源組名。</span><span class="sxs-lookup"><span data-stu-id="339ce-116">The resource group name.</span></span>

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

### <span data-ttu-id="339ce-117">-確認</span><span class="sxs-lookup"><span data-stu-id="339ce-117">-Confirm</span></span>
<span data-ttu-id="339ce-118">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="339ce-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="339ce-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="339ce-119">-WhatIf</span></span>
<span data-ttu-id="339ce-120">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="339ce-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="339ce-121">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="339ce-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="339ce-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="339ce-122">CommonParameters</span></span>
<span data-ttu-id="339ce-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="339ce-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="339ce-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="339ce-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="339ce-125">輸入</span><span class="sxs-lookup"><span data-stu-id="339ce-125">INPUTS</span></span>

### <span data-ttu-id="339ce-126">System.String</span><span class="sxs-lookup"><span data-stu-id="339ce-126">System.String</span></span>

## <span data-ttu-id="339ce-127">輸出</span><span class="sxs-lookup"><span data-stu-id="339ce-127">OUTPUTS</span></span>

### <span data-ttu-id="339ce-128">Microsoft.Azure.Commands.Network.models.PS VpnProfile</span><span class="sxs-lookup"><span data-stu-id="339ce-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="339ce-129">筆記</span><span class="sxs-lookup"><span data-stu-id="339ce-129">NOTES</span></span>

## <span data-ttu-id="339ce-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="339ce-130">RELATED LINKS</span></span>

[<span data-ttu-id="339ce-131">New-Az VpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="339ce-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)
