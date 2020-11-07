---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityContact.md
ms.openlocfilehash: 3d27e9a7962e20dff0d6360eb11db6a49c61a06d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625244"
---
# <span data-ttu-id="8271b-101">Get-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="8271b-101">Get-AzureRmSecurityContact</span></span>

## <span data-ttu-id="8271b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8271b-102">SYNOPSIS</span></span>
<span data-ttu-id="8271b-103">取得此訂閱上設定的安全連絡人</span><span class="sxs-lookup"><span data-stu-id="8271b-103">Gets security contacts that were configured on this subscription</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8271b-104">句法</span><span class="sxs-lookup"><span data-stu-id="8271b-104">SYNTAX</span></span>

### <span data-ttu-id="8271b-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="8271b-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8271b-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="8271b-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8271b-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="8271b-107">ResourceId</span></span>
```
Get-AzureRmSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8271b-108">說明</span><span class="sxs-lookup"><span data-stu-id="8271b-108">DESCRIPTION</span></span>
<span data-ttu-id="8271b-109">取得此訂閱上設定的安全連絡人。</span><span class="sxs-lookup"><span data-stu-id="8271b-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="8271b-110">安全連絡人可以取得訂閱上所發生之安全警報的通知。</span><span class="sxs-lookup"><span data-stu-id="8271b-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="8271b-111">示例</span><span class="sxs-lookup"><span data-stu-id="8271b-111">EXAMPLES</span></span>

### <span data-ttu-id="8271b-112">範例1</span><span class="sxs-lookup"><span data-stu-id="8271b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="8271b-113">取得訂閱上所有已設定的安全性連絡人</span><span class="sxs-lookup"><span data-stu-id="8271b-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="8271b-114">參數</span><span class="sxs-lookup"><span data-stu-id="8271b-114">PARAMETERS</span></span>

### <span data-ttu-id="8271b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8271b-115">-DefaultProfile</span></span>
<span data-ttu-id="8271b-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8271b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8271b-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="8271b-117">-Name</span></span>
<span data-ttu-id="8271b-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="8271b-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8271b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8271b-119">-ResourceId</span></span>
<span data-ttu-id="8271b-120">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="8271b-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8271b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8271b-121">CommonParameters</span></span>
<span data-ttu-id="8271b-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8271b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8271b-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8271b-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8271b-124">輸入</span><span class="sxs-lookup"><span data-stu-id="8271b-124">INPUTS</span></span>

### <span data-ttu-id="8271b-125">System.object</span><span class="sxs-lookup"><span data-stu-id="8271b-125">System.String</span></span>

## <span data-ttu-id="8271b-126">輸出</span><span class="sxs-lookup"><span data-stu-id="8271b-126">OUTPUTS</span></span>

### <span data-ttu-id="8271b-127">PSSecurityContact 中的 SecurityContacts （Security..。</span><span class="sxs-lookup"><span data-stu-id="8271b-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="8271b-128">筆記</span><span class="sxs-lookup"><span data-stu-id="8271b-128">NOTES</span></span>

## <span data-ttu-id="8271b-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="8271b-129">RELATED LINKS</span></span>
