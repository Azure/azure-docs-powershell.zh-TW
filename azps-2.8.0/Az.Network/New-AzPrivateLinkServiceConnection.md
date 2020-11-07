---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivatelinkserviceconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateLinkServiceConnection.md
ms.openlocfilehash: 8669eed6e34b2f03d4da8f1f6490a95e4762241d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93790790"
---
# <span data-ttu-id="31518-101">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="31518-101">New-AzPrivateLinkServiceConnection</span></span>

## <span data-ttu-id="31518-102">摘要</span><span class="sxs-lookup"><span data-stu-id="31518-102">SYNOPSIS</span></span>
<span data-ttu-id="31518-103">建立私人連結服務連線設定。</span><span class="sxs-lookup"><span data-stu-id="31518-103">Creates a private link service connection configuration.</span></span>

## <span data-ttu-id="31518-104">句法</span><span class="sxs-lookup"><span data-stu-id="31518-104">SYNTAX</span></span>

### <span data-ttu-id="31518-105">SetByResource (預設) </span><span class="sxs-lookup"><span data-stu-id="31518-105">SetByResource (Default)</span></span>
```
New-AzPrivateLinkServiceConnection -Name <String> -PrivateLinkService <PSPrivateLinkService>
 [-GroupId <String[]>] [-RequestMessage <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="31518-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="31518-106">SetByResourceId</span></span>
```
New-AzPrivateLinkServiceConnection -Name <String> -PrivateLinkServiceId <String> [-GroupId <String[]>]
 [-RequestMessage <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31518-107">說明</span><span class="sxs-lookup"><span data-stu-id="31518-107">DESCRIPTION</span></span>
<span data-ttu-id="31518-108">**新的-AzPrivateLinkServiceConnection** Cmdlet 會建立私人連結服務連線設定。</span><span class="sxs-lookup"><span data-stu-id="31518-108">**The New-AzPrivateLinkServiceConnection** cmdlet creates a private link service connection configuration.</span></span>

## <span data-ttu-id="31518-109">示例</span><span class="sxs-lookup"><span data-stu-id="31518-109">EXAMPLES</span></span>

### <span data-ttu-id="31518-110">範例1</span><span class="sxs-lookup"><span data-stu-id="31518-110">Example 1</span></span>
```
New-AzPrivateLinkServiceConnection -Name MyPLSConnection -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
```

<span data-ttu-id="31518-111">這個範例會在記憶體中建立私人連結服務連線物件，以便在建立私人端點時使用。</span><span class="sxs-lookup"><span data-stu-id="31518-111">This example create a private link service connection object in memory for using in creating private endpoint.</span></span>

## <span data-ttu-id="31518-112">參數</span><span class="sxs-lookup"><span data-stu-id="31518-112">PARAMETERS</span></span>

### <span data-ttu-id="31518-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31518-113">-DefaultProfile</span></span>
<span data-ttu-id="31518-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="31518-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31518-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="31518-115">-GroupId</span></span>
<span data-ttu-id="31518-116">群組識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="31518-116">The list of group id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31518-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="31518-117">-Name</span></span>
<span data-ttu-id="31518-118">私人連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="31518-118">The name of private link service.</span></span>

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

### <span data-ttu-id="31518-119">-PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="31518-119">-PrivateLinkService</span></span>
<span data-ttu-id="31518-120">私人連結服務。</span><span class="sxs-lookup"><span data-stu-id="31518-120">The private link service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkService
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31518-121">-PrivateLinkServiceId</span><span class="sxs-lookup"><span data-stu-id="31518-121">-PrivateLinkServiceId</span></span>
<span data-ttu-id="31518-122">私人連結服務的 id。</span><span class="sxs-lookup"><span data-stu-id="31518-122">The id of private link service.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31518-123">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="31518-123">-RequestMessage</span></span>
<span data-ttu-id="31518-124">[要求] 訊息。</span><span class="sxs-lookup"><span data-stu-id="31518-124">The request message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31518-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31518-125">CommonParameters</span></span>
<span data-ttu-id="31518-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="31518-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31518-127">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="31518-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31518-128">輸入</span><span class="sxs-lookup"><span data-stu-id="31518-128">INPUTS</span></span>

### <span data-ttu-id="31518-129">所有</span><span class="sxs-lookup"><span data-stu-id="31518-129">None</span></span>

## <span data-ttu-id="31518-130">輸出</span><span class="sxs-lookup"><span data-stu-id="31518-130">OUTPUTS</span></span>

### <span data-ttu-id="31518-131">PSPrivateLinkServiceConnection 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="31518-131">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection</span></span>

## <span data-ttu-id="31518-132">筆記</span><span class="sxs-lookup"><span data-stu-id="31518-132">NOTES</span></span>

## <span data-ttu-id="31518-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="31518-133">RELATED LINKS</span></span>

[<span data-ttu-id="31518-134">新-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="31518-134">New-AzPrivateEndpoint</span></span>](./New-AzPrivateEndpoint.md)