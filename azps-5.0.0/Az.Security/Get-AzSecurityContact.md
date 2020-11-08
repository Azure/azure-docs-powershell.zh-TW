---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
ms.openlocfilehash: b1f01c880781ef485b29a7072f8ca6ff17c65d4a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139621"
---
# <span data-ttu-id="ba2ad-101">Get-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="ba2ad-101">Get-AzSecurityContact</span></span>

## <span data-ttu-id="ba2ad-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ba2ad-102">SYNOPSIS</span></span>
<span data-ttu-id="ba2ad-103">取得此訂閱上設定的安全連絡人</span><span class="sxs-lookup"><span data-stu-id="ba2ad-103">Gets security contacts that were configured on this subscription</span></span>

## <span data-ttu-id="ba2ad-104">句法</span><span class="sxs-lookup"><span data-stu-id="ba2ad-104">SYNTAX</span></span>

### <span data-ttu-id="ba2ad-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="ba2ad-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba2ad-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="ba2ad-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba2ad-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba2ad-107">ResourceId</span></span>
```
Get-AzSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba2ad-108">說明</span><span class="sxs-lookup"><span data-stu-id="ba2ad-108">DESCRIPTION</span></span>
<span data-ttu-id="ba2ad-109">取得此訂閱上設定的安全連絡人。</span><span class="sxs-lookup"><span data-stu-id="ba2ad-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="ba2ad-110">安全連絡人可以取得訂閱上所發生之安全警報的通知。</span><span class="sxs-lookup"><span data-stu-id="ba2ad-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="ba2ad-111">示例</span><span class="sxs-lookup"><span data-stu-id="ba2ad-111">EXAMPLES</span></span>

### <span data-ttu-id="ba2ad-112">範例1</span><span class="sxs-lookup"><span data-stu-id="ba2ad-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="ba2ad-113">取得訂閱上所有已設定的安全性連絡人</span><span class="sxs-lookup"><span data-stu-id="ba2ad-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="ba2ad-114">參數</span><span class="sxs-lookup"><span data-stu-id="ba2ad-114">PARAMETERS</span></span>

### <span data-ttu-id="ba2ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba2ad-115">-DefaultProfile</span></span>
<span data-ttu-id="ba2ad-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ba2ad-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba2ad-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="ba2ad-117">-Name</span></span>
<span data-ttu-id="ba2ad-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="ba2ad-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba2ad-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba2ad-119">-ResourceId</span></span>
<span data-ttu-id="ba2ad-120">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="ba2ad-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba2ad-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba2ad-121">CommonParameters</span></span>
<span data-ttu-id="ba2ad-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ba2ad-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba2ad-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ba2ad-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba2ad-124">輸入</span><span class="sxs-lookup"><span data-stu-id="ba2ad-124">INPUTS</span></span>

### <span data-ttu-id="ba2ad-125">System.object</span><span class="sxs-lookup"><span data-stu-id="ba2ad-125">System.String</span></span>

## <span data-ttu-id="ba2ad-126">輸出</span><span class="sxs-lookup"><span data-stu-id="ba2ad-126">OUTPUTS</span></span>

### <span data-ttu-id="ba2ad-127">PSSecurityContact 中的 SecurityContacts （Security..。</span><span class="sxs-lookup"><span data-stu-id="ba2ad-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="ba2ad-128">筆記</span><span class="sxs-lookup"><span data-stu-id="ba2ad-128">NOTES</span></span>

## <span data-ttu-id="ba2ad-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="ba2ad-129">RELATED LINKS</span></span>