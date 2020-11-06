---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
ms.openlocfilehash: 342c18add7438c75babd1225722c3830c4c5c696
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445516"
---
# <span data-ttu-id="c8d08-101">Get-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="c8d08-101">Get-AzureRmWcfRelay</span></span>

## <span data-ttu-id="c8d08-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c8d08-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d08-103">傳回指定 WcfRelay 的描述。</span><span class="sxs-lookup"><span data-stu-id="c8d08-103">Returns a description for the specified WcfRelay.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8d08-104">句法</span><span class="sxs-lookup"><span data-stu-id="c8d08-104">SYNTAX</span></span>

```
Get-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8d08-105">說明</span><span class="sxs-lookup"><span data-stu-id="c8d08-105">DESCRIPTION</span></span>
<span data-ttu-id="c8d08-106">**AzureRmWcfRelay** Cmdlet 會傳回指定 WcfRelay 的描述。</span><span class="sxs-lookup"><span data-stu-id="c8d08-106">The **Get-AzureRmWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="c8d08-107">示例</span><span class="sxs-lookup"><span data-stu-id="c8d08-107">EXAMPLES</span></span>

### <span data-ttu-id="c8d08-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c8d08-108">Example 1</span></span>
```
PS C:\> Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1

RelayType                   : NetTcp
CreatedAt                   : 4/12/2017 2:23:08 AM
UpdatedAt                   : 4/12/2017 2:23:08 AM
ListenerCount               : 0
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W
                              cfRelays/TestWCFRelay1
Name                        : TestWCFRelay1
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="c8d08-109">傳回 WcfRelay 的描述。</span><span class="sxs-lookup"><span data-stu-id="c8d08-109">Returns the description of the WcfRelay.</span></span>

## <span data-ttu-id="c8d08-110">參數</span><span class="sxs-lookup"><span data-stu-id="c8d08-110">PARAMETERS</span></span>

### <span data-ttu-id="c8d08-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8d08-111">-DefaultProfile</span></span>
<span data-ttu-id="c8d08-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c8d08-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8d08-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="c8d08-113">-Name</span></span>
<span data-ttu-id="c8d08-114">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="c8d08-114">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8d08-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="c8d08-115">-Namespace</span></span>
<span data-ttu-id="c8d08-116">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="c8d08-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8d08-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8d08-117">-ResourceGroupName</span></span>
<span data-ttu-id="c8d08-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="c8d08-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8d08-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d08-119">CommonParameters</span></span>
<span data-ttu-id="c8d08-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c8d08-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c8d08-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c8d08-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d08-122">輸入</span><span class="sxs-lookup"><span data-stu-id="c8d08-122">INPUTS</span></span>

### <span data-ttu-id="c8d08-123">System.object</span><span class="sxs-lookup"><span data-stu-id="c8d08-123">System.String</span></span>


## <span data-ttu-id="c8d08-124">輸出</span><span class="sxs-lookup"><span data-stu-id="c8d08-124">OUTPUTS</span></span>

### <span data-ttu-id="c8d08-125">PSWcfRelayAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c8d08-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>


## <span data-ttu-id="c8d08-126">筆記</span><span class="sxs-lookup"><span data-stu-id="c8d08-126">NOTES</span></span>

## <span data-ttu-id="c8d08-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="c8d08-127">RELATED LINKS</span></span>
