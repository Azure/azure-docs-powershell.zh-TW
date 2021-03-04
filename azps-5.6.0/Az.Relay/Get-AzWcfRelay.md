---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/get-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
ms.openlocfilehash: e998bb09435abc787df78050ab25888d0e6651a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914601"
---
# <span data-ttu-id="0bed8-101">Get-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="0bed8-101">Get-AzWcfRelay</span></span>

## <span data-ttu-id="0bed8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0bed8-102">SYNOPSIS</span></span>
<span data-ttu-id="0bed8-103">會針對指定的 WcfRelay 返回描述。</span><span class="sxs-lookup"><span data-stu-id="0bed8-103">Returns a description for the specified WcfRelay.</span></span>

## <span data-ttu-id="0bed8-104">語法</span><span class="sxs-lookup"><span data-stu-id="0bed8-104">SYNTAX</span></span>

```
Get-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bed8-105">描述</span><span class="sxs-lookup"><span data-stu-id="0bed8-105">DESCRIPTION</span></span>
<span data-ttu-id="0bed8-106">**Get-AzWcfRelay Cmdlet** 會返回指定 WcfRelay 的描述。</span><span class="sxs-lookup"><span data-stu-id="0bed8-106">The **Get-AzWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="0bed8-107">例子</span><span class="sxs-lookup"><span data-stu-id="0bed8-107">EXAMPLES</span></span>

### <span data-ttu-id="0bed8-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="0bed8-108">Example 1</span></span>
```
PS C:\> Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1

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

<span data-ttu-id="0bed8-109">會返回 WcfRelay 的描述。</span><span class="sxs-lookup"><span data-stu-id="0bed8-109">Returns the description of the WcfRelay.</span></span>

## <span data-ttu-id="0bed8-110">參數</span><span class="sxs-lookup"><span data-stu-id="0bed8-110">PARAMETERS</span></span>

### <span data-ttu-id="0bed8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bed8-111">-DefaultProfile</span></span>
<span data-ttu-id="0bed8-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0bed8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bed8-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="0bed8-113">-Name</span></span>
<span data-ttu-id="0bed8-114">WcfRelay 名稱。</span><span class="sxs-lookup"><span data-stu-id="0bed8-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="0bed8-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="0bed8-115">-Namespace</span></span>
<span data-ttu-id="0bed8-116">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="0bed8-116">Namespace Name.</span></span>

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

### <span data-ttu-id="0bed8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bed8-117">-ResourceGroupName</span></span>
<span data-ttu-id="0bed8-118">資源組名。</span><span class="sxs-lookup"><span data-stu-id="0bed8-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="0bed8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bed8-119">CommonParameters</span></span>
<span data-ttu-id="0bed8-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0bed8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bed8-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0bed8-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bed8-122">輸入</span><span class="sxs-lookup"><span data-stu-id="0bed8-122">INPUTS</span></span>

### <span data-ttu-id="0bed8-123">System.String</span><span class="sxs-lookup"><span data-stu-id="0bed8-123">System.String</span></span>

## <span data-ttu-id="0bed8-124">輸出</span><span class="sxs-lookup"><span data-stu-id="0bed8-124">OUTPUTS</span></span>

### <span data-ttu-id="0bed8-125">Microsoft.Azure.Commands.Relay.models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="0bed8-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="0bed8-126">筆記</span><span class="sxs-lookup"><span data-stu-id="0bed8-126">NOTES</span></span>

## <span data-ttu-id="0bed8-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="0bed8-127">RELATED LINKS</span></span>
