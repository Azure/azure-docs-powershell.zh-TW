---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 3442c5a16493d42dbbfd6460f398b37bb92d6d72
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789033"
---
# <span data-ttu-id="d66f5-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d66f5-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="d66f5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d66f5-102">SYNOPSIS</span></span>
<span data-ttu-id="d66f5-103">更新應用程式閘道防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="d66f5-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="d66f5-104">句法</span><span class="sxs-lookup"><span data-stu-id="d66f5-104">SYNTAX</span></span>

### <span data-ttu-id="d66f5-105">ByFactoryObject (預設) </span><span class="sxs-lookup"><span data-stu-id="d66f5-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d66f5-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="d66f5-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d66f5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d66f5-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d66f5-108">說明</span><span class="sxs-lookup"><span data-stu-id="d66f5-108">DESCRIPTION</span></span>
<span data-ttu-id="d66f5-109">**AzApplicationGatewayFirewallPolicy** Cmdlet 會更新 Azure 應用程式閘道防火牆原則。</span><span class="sxs-lookup"><span data-stu-id="d66f5-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="d66f5-110">示例</span><span class="sxs-lookup"><span data-stu-id="d66f5-110">EXAMPLES</span></span>

### <span data-ttu-id="d66f5-111">範例1</span><span class="sxs-lookup"><span data-stu-id="d66f5-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="d66f5-112">這個命令會使用 $AppGwFirewallPolicy 變數中的設定來更新應用程式閘道防火牆原則，並將更新的閘道儲存在 $UpdatedAppGwFirewallPolicy 變數中。</span><span class="sxs-lookup"><span data-stu-id="d66f5-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="d66f5-113">參數</span><span class="sxs-lookup"><span data-stu-id="d66f5-113">PARAMETERS</span></span>

### <span data-ttu-id="d66f5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d66f5-114">-AsJob</span></span>
<span data-ttu-id="d66f5-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d66f5-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d66f5-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="d66f5-116">-CustomRule</span></span>
<span data-ttu-id="d66f5-117">CustomRules 清單</span><span class="sxs-lookup"><span data-stu-id="d66f5-117">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d66f5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d66f5-118">-DefaultProfile</span></span>
<span data-ttu-id="d66f5-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d66f5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d66f5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d66f5-120">-InputObject</span></span>
<span data-ttu-id="d66f5-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d66f5-121">The applicationGatewayFirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d66f5-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="d66f5-122">-Name</span></span>
<span data-ttu-id="d66f5-123">防火牆原則名稱。</span><span class="sxs-lookup"><span data-stu-id="d66f5-123">The Firewall Policy Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66f5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d66f5-124">-ResourceGroupName</span></span>
<span data-ttu-id="d66f5-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d66f5-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d66f5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d66f5-126">-ResourceId</span></span>
<span data-ttu-id="d66f5-127">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d66f5-127">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d66f5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d66f5-128">CommonParameters</span></span>
<span data-ttu-id="d66f5-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d66f5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d66f5-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d66f5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d66f5-131">輸入</span><span class="sxs-lookup"><span data-stu-id="d66f5-131">INPUTS</span></span>

### <span data-ttu-id="d66f5-132">PSApplicationGatewayWebApplicationFirewallPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d66f5-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="d66f5-133">輸出</span><span class="sxs-lookup"><span data-stu-id="d66f5-133">OUTPUTS</span></span>

### <span data-ttu-id="d66f5-134">PSApplicationGatewayWebApplicationFirewallPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="d66f5-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="d66f5-135">筆記</span><span class="sxs-lookup"><span data-stu-id="d66f5-135">NOTES</span></span>

## <span data-ttu-id="d66f5-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="d66f5-136">RELATED LINKS</span></span>
