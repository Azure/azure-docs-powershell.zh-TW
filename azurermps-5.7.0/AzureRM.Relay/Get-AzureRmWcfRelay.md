---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
ms.openlocfilehash: 88d2c8f7b0bcab3faad6368070606b8a36948343
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454152"
---
# <span data-ttu-id="4591f-101">Get-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="4591f-101">Get-AzureRmWcfRelay</span></span>

## <span data-ttu-id="4591f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4591f-102">SYNOPSIS</span></span>
<span data-ttu-id="4591f-103">傳回指定 WcfRelay 的描述。</span><span class="sxs-lookup"><span data-stu-id="4591f-103">Returns a description for the specified WcfRelay.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4591f-104">句法</span><span class="sxs-lookup"><span data-stu-id="4591f-104">SYNTAX</span></span>

```
Get-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4591f-105">說明</span><span class="sxs-lookup"><span data-stu-id="4591f-105">DESCRIPTION</span></span>
<span data-ttu-id="4591f-106">**AzureRmWcfRelay** Cmdlet 會傳回指定 WcfRelay 的描述。</span><span class="sxs-lookup"><span data-stu-id="4591f-106">The **Get-AzureRmWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="4591f-107">示例</span><span class="sxs-lookup"><span data-stu-id="4591f-107">EXAMPLES</span></span>

### <span data-ttu-id="4591f-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4591f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="4591f-109">傳回 WcfRelay 的描述。</span><span class="sxs-lookup"><span data-stu-id="4591f-109">Returns the description of the WcfRelay.</span></span> 

## <span data-ttu-id="4591f-110">參數</span><span class="sxs-lookup"><span data-stu-id="4591f-110">PARAMETERS</span></span>

### <span data-ttu-id="4591f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4591f-111">-DefaultProfile</span></span>
<span data-ttu-id="4591f-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4591f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4591f-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="4591f-113">-Name</span></span>
<span data-ttu-id="4591f-114">WcfRelay [名稱]。</span><span class="sxs-lookup"><span data-stu-id="4591f-114">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4591f-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="4591f-115">-Namespace</span></span>
<span data-ttu-id="4591f-116">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="4591f-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4591f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4591f-117">-ResourceGroupName</span></span>
<span data-ttu-id="4591f-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="4591f-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4591f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4591f-119">CommonParameters</span></span>
<span data-ttu-id="4591f-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4591f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4591f-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4591f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4591f-122">輸入</span><span class="sxs-lookup"><span data-stu-id="4591f-122">INPUTS</span></span>

### <span data-ttu-id="4591f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4591f-123">-ResourceGroupName</span></span>
 <span data-ttu-id="4591f-124">System.object</span><span class="sxs-lookup"><span data-stu-id="4591f-124">System.String</span></span>
 

### <span data-ttu-id="4591f-125">-命名空間</span><span class="sxs-lookup"><span data-stu-id="4591f-125">-Namespace</span></span>
 <span data-ttu-id="4591f-126">System.object</span><span class="sxs-lookup"><span data-stu-id="4591f-126">System.String</span></span>
 

### <span data-ttu-id="4591f-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="4591f-127">-Name</span></span>
 <span data-ttu-id="4591f-128">System.object</span><span class="sxs-lookup"><span data-stu-id="4591f-128">System.String</span></span> 

## <span data-ttu-id="4591f-129">輸出</span><span class="sxs-lookup"><span data-stu-id="4591f-129">OUTPUTS</span></span>

### <span data-ttu-id="4591f-130">[System.object]. 清單 ' 1 [WcfRelayAttributes，0.1.0.0，#.. 繼電器，版本 =，Culture = 中性，PublicKeyToken = null]]。</span><span class="sxs-lookup"><span data-stu-id="4591f-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="4591f-131">RelayType： NetTcp CreatedAt： 4/12/2017 2:23:08 AM UpdatedAt： 4/12/2017 2:23:08 AM ListenerCount： 0 RequiresClientAuthorization： True RequiresTransportSecurity： True IsDynamic： False UserMetadata： User 中繼資料 Id：/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 Name： TestWCFRelay1 類型： Microsoft. 中繼/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="4591f-131">RelayType                   : NetTcp CreatedAt                   : 4/12/2017 2:23:08 AM UpdatedAt                   : 4/12/2017 2:23:08 AM ListenerCount               : 0 RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 Name                        : TestWCFRelay1 Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="4591f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="4591f-132">NOTES</span></span>

## <span data-ttu-id="4591f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="4591f-133">RELATED LINKS</span></span>

