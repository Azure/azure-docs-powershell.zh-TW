---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
ms.openlocfilehash: 260cb8b605415137e9a9e667634ff02b8d4b3de7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283752"
---
# <span data-ttu-id="f7622-101">Get-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="f7622-101">Get-AzWcfRelay</span></span>

## <span data-ttu-id="f7622-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7622-102">SYNOPSIS</span></span>
<span data-ttu-id="f7622-103">傳回指定 WcfRelay 的描述。</span><span class="sxs-lookup"><span data-stu-id="f7622-103">Returns a description for the specified WcfRelay.</span></span>

## <span data-ttu-id="f7622-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7622-104">SYNTAX</span></span>

```
Get-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7622-105">說明</span><span class="sxs-lookup"><span data-stu-id="f7622-105">DESCRIPTION</span></span>
<span data-ttu-id="f7622-106">**AzWcfRelay** Cmdlet 會傳回指定 WcfRelay 的描述。</span><span class="sxs-lookup"><span data-stu-id="f7622-106">The **Get-AzWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="f7622-107">示例</span><span class="sxs-lookup"><span data-stu-id="f7622-107">EXAMPLES</span></span>

### <span data-ttu-id="f7622-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f7622-108">Example 1</span></span>
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

<span data-ttu-id="f7622-109">傳回 WcfRelay 的描述。</span><span class="sxs-lookup"><span data-stu-id="f7622-109">Returns the description of the WcfRelay.</span></span>

## <span data-ttu-id="f7622-110">參數</span><span class="sxs-lookup"><span data-stu-id="f7622-110">PARAMETERS</span></span>

### <span data-ttu-id="f7622-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7622-111">-DefaultProfile</span></span>
<span data-ttu-id="f7622-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7622-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7622-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7622-113">-Name</span></span>
<span data-ttu-id="f7622-114">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="f7622-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="f7622-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="f7622-115">-Namespace</span></span>
<span data-ttu-id="f7622-116">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="f7622-116">Namespace Name.</span></span>

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

### <span data-ttu-id="f7622-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7622-117">-ResourceGroupName</span></span>
<span data-ttu-id="f7622-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f7622-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="f7622-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7622-119">CommonParameters</span></span>
<span data-ttu-id="f7622-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7622-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7622-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7622-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7622-122">輸入</span><span class="sxs-lookup"><span data-stu-id="f7622-122">INPUTS</span></span>

### <span data-ttu-id="f7622-123">System.object</span><span class="sxs-lookup"><span data-stu-id="f7622-123">System.String</span></span>

## <span data-ttu-id="f7622-124">輸出</span><span class="sxs-lookup"><span data-stu-id="f7622-124">OUTPUTS</span></span>

### <span data-ttu-id="f7622-125">PSWcfRelayAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="f7622-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="f7622-126">筆記</span><span class="sxs-lookup"><span data-stu-id="f7622-126">NOTES</span></span>

## <span data-ttu-id="f7622-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7622-127">RELATED LINKS</span></span>
