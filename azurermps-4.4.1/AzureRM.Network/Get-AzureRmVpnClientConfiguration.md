---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: 7050e348530231d9ecc7fbec443f15238f6a41f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626602"
---
# <span data-ttu-id="bb8bf-101">Get-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb8bf-101">Get-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="bb8bf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bb8bf-102">SYNOPSIS</span></span>
<span data-ttu-id="bb8bf-103">讓使用者能夠輕鬆下載使用 New-AzureRmVpnClientConfiguration commandlet 所產生的 Vpn 設定檔套件。</span><span class="sxs-lookup"><span data-stu-id="bb8bf-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzureRmVpnClientConfiguration commandlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb8bf-104">句法</span><span class="sxs-lookup"><span data-stu-id="bb8bf-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb8bf-105">說明</span><span class="sxs-lookup"><span data-stu-id="bb8bf-105">DESCRIPTION</span></span>
<span data-ttu-id="bb8bf-106">{{填入描述}}</span><span class="sxs-lookup"><span data-stu-id="bb8bf-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="bb8bf-107">示例</span><span class="sxs-lookup"><span data-stu-id="bb8bf-107">EXAMPLES</span></span>

### <span data-ttu-id="bb8bf-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bb8bf-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="bb8bf-109">取得 URL 以下載先前使用 New-AzureRMVpnClientConfiguration 命令產生的 VpnClient 設定檔。</span><span class="sxs-lookup"><span data-stu-id="bb8bf-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzureRMVpnClientConfiguration command.</span></span>

## <span data-ttu-id="bb8bf-110">參數</span><span class="sxs-lookup"><span data-stu-id="bb8bf-110">PARAMETERS</span></span>

### <span data-ttu-id="bb8bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb8bf-111">-DefaultProfile</span></span>
<span data-ttu-id="bb8bf-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bb8bf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="bb8bf-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="bb8bf-113">-Name</span></span>
<span data-ttu-id="bb8bf-114">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="bb8bf-114">The resource name.</span></span>

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

### <span data-ttu-id="bb8bf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb8bf-115">-ResourceGroupName</span></span>
<span data-ttu-id="bb8bf-116">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bb8bf-116">The resource group name.</span></span>

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

### <span data-ttu-id="bb8bf-117">-確認</span><span class="sxs-lookup"><span data-stu-id="bb8bf-117">-Confirm</span></span>
<span data-ttu-id="bb8bf-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bb8bf-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb8bf-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb8bf-119">-WhatIf</span></span>
<span data-ttu-id="bb8bf-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bb8bf-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bb8bf-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bb8bf-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb8bf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb8bf-122">CommonParameters</span></span>
<span data-ttu-id="bb8bf-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bb8bf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb8bf-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bb8bf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb8bf-125">輸入</span><span class="sxs-lookup"><span data-stu-id="bb8bf-125">INPUTS</span></span>

### <span data-ttu-id="bb8bf-126">System.object</span><span class="sxs-lookup"><span data-stu-id="bb8bf-126">System.String</span></span>

## <span data-ttu-id="bb8bf-127">輸出</span><span class="sxs-lookup"><span data-stu-id="bb8bf-127">OUTPUTS</span></span>

### <span data-ttu-id="bb8bf-128">PSVpnProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="bb8bf-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="bb8bf-129">筆記</span><span class="sxs-lookup"><span data-stu-id="bb8bf-129">NOTES</span></span>

## <span data-ttu-id="bb8bf-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="bb8bf-130">RELATED LINKS</span></span>

