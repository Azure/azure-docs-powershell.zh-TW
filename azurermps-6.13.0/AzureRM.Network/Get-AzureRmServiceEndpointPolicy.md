---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 989b6aa91c0dabec1b72425f214c4097df374041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447356"
---
# <span data-ttu-id="46aa6-101">Get-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="46aa6-101">Get-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="46aa6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="46aa6-102">SYNOPSIS</span></span>
<span data-ttu-id="46aa6-103">{{填入摘要}}</span><span class="sxs-lookup"><span data-stu-id="46aa6-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46aa6-104">句法</span><span class="sxs-lookup"><span data-stu-id="46aa6-104">SYNTAX</span></span>

```
Get-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46aa6-105">說明</span><span class="sxs-lookup"><span data-stu-id="46aa6-105">DESCRIPTION</span></span>
<span data-ttu-id="46aa6-106">**AzureRmServiceEndpointPolicy** Cmdlet 會取得服務端點原則。</span><span class="sxs-lookup"><span data-stu-id="46aa6-106">The **Get-AzureRmServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="46aa6-107">示例</span><span class="sxs-lookup"><span data-stu-id="46aa6-107">EXAMPLES</span></span>

### <span data-ttu-id="46aa6-108">範例1</span><span class="sxs-lookup"><span data-stu-id="46aa6-108">Example 1</span></span>
```
$policy = Get-AzureRmServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="46aa6-109">這個命令會取得屬於名為 ResourceGroup01 之資源群組的名為 ServiceEndpointPolicy1 的服務端點原則，並將它儲存在 $policy 變數中。</span><span class="sxs-lookup"><span data-stu-id="46aa6-109">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="46aa6-110">範例2</span><span class="sxs-lookup"><span data-stu-id="46aa6-110">Example 2</span></span>
```
$policyList = Get-AzureRmServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="46aa6-111">這個命令會在名為 ResourceGroup01 的資源群組中取得所有服務端點原則的清單，並將它儲存在 $policyList 變數中。</span><span class="sxs-lookup"><span data-stu-id="46aa6-111">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

## <span data-ttu-id="46aa6-112">參數</span><span class="sxs-lookup"><span data-stu-id="46aa6-112">PARAMETERS</span></span>

### <span data-ttu-id="46aa6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46aa6-113">-DefaultProfile</span></span>
<span data-ttu-id="46aa6-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="46aa6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46aa6-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="46aa6-115">-Name</span></span>
<span data-ttu-id="46aa6-116">服務端點原則的名稱</span><span class="sxs-lookup"><span data-stu-id="46aa6-116">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46aa6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46aa6-117">-ResourceGroupName</span></span>
<span data-ttu-id="46aa6-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="46aa6-118">The resource group name.</span></span>

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

### <span data-ttu-id="46aa6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46aa6-119">CommonParameters</span></span>
<span data-ttu-id="46aa6-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="46aa6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="46aa6-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="46aa6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46aa6-122">輸入</span><span class="sxs-lookup"><span data-stu-id="46aa6-122">INPUTS</span></span>

### <span data-ttu-id="46aa6-123">System.object</span><span class="sxs-lookup"><span data-stu-id="46aa6-123">System.String</span></span>


## <span data-ttu-id="46aa6-124">輸出</span><span class="sxs-lookup"><span data-stu-id="46aa6-124">OUTPUTS</span></span>

### <span data-ttu-id="46aa6-125">PSServiceEndpointPolicy 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="46aa6-125">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="46aa6-126">筆記</span><span class="sxs-lookup"><span data-stu-id="46aa6-126">NOTES</span></span>

## <span data-ttu-id="46aa6-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="46aa6-127">RELATED LINKS</span></span>
