---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
ms.openlocfilehash: 7dab3fd72dcd7ac097dbf5a1d5da342c39d3c504
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792281"
---
# <span data-ttu-id="39264-101">Get-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="39264-101">Get-AzRelayHybridConnection</span></span>

## <span data-ttu-id="39264-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39264-102">SYNOPSIS</span></span>
<span data-ttu-id="39264-103">取得中繼命名空間中指定 HybridConnection 的描述。</span><span class="sxs-lookup"><span data-stu-id="39264-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="39264-104">句法</span><span class="sxs-lookup"><span data-stu-id="39264-104">SYNTAX</span></span>

```
Get-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39264-105">說明</span><span class="sxs-lookup"><span data-stu-id="39264-105">DESCRIPTION</span></span>
<span data-ttu-id="39264-106">**AzRelayHybridConnection** Cmdlet 會取得中繼命名空間中指定 HybridConnection 的描述。</span><span class="sxs-lookup"><span data-stu-id="39264-106">The **Get-AzRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="39264-107">示例</span><span class="sxs-lookup"><span data-stu-id="39264-107">EXAMPLES</span></span>

### <span data-ttu-id="39264-108">範例1</span><span class="sxs-lookup"><span data-stu-id="39264-108">Example 1</span></span>
```
PS C:\>Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection

CreatedAt                   : 4/12/2017 3:17:02 AM
UpdatedAt                   : 4/12/2017 3:17:02 AM
ListenerCount               : 0
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H
                              ybridConnections/TestHybridConnection
Name                        : TestHybridConnection
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="39264-109">傳回 HybridConnection 的描述。</span><span class="sxs-lookup"><span data-stu-id="39264-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="39264-110">參數</span><span class="sxs-lookup"><span data-stu-id="39264-110">PARAMETERS</span></span>

### <span data-ttu-id="39264-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39264-111">-DefaultProfile</span></span>
<span data-ttu-id="39264-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="39264-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39264-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="39264-113">-Name</span></span>
<span data-ttu-id="39264-114">HybridConnections [名稱]。</span><span class="sxs-lookup"><span data-stu-id="39264-114">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39264-115">-命名空間</span><span class="sxs-lookup"><span data-stu-id="39264-115">-Namespace</span></span>
<span data-ttu-id="39264-116">命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="39264-116">Namespace Name.</span></span>

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

### <span data-ttu-id="39264-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39264-117">-ResourceGroupName</span></span>
<span data-ttu-id="39264-118">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="39264-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="39264-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39264-119">CommonParameters</span></span>
<span data-ttu-id="39264-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39264-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39264-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="39264-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39264-122">輸入</span><span class="sxs-lookup"><span data-stu-id="39264-122">INPUTS</span></span>

### <span data-ttu-id="39264-123">System.object</span><span class="sxs-lookup"><span data-stu-id="39264-123">System.String</span></span>

## <span data-ttu-id="39264-124">輸出</span><span class="sxs-lookup"><span data-stu-id="39264-124">OUTPUTS</span></span>

### <span data-ttu-id="39264-125">PSHybridConnectionAttributes 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="39264-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="39264-126">筆記</span><span class="sxs-lookup"><span data-stu-id="39264-126">NOTES</span></span>

## <span data-ttu-id="39264-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="39264-127">RELATED LINKS</span></span>
