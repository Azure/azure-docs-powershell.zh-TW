---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityContact.md
ms.openlocfilehash: a00edef30c327e9bce4e2fa008dad373a2e6367d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908757"
---
# <span data-ttu-id="2f720-101">Get-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="2f720-101">Get-AzSecurityContact</span></span>

## <span data-ttu-id="2f720-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2f720-102">SYNOPSIS</span></span>
<span data-ttu-id="2f720-103">獲得此訂閱上所配置的安全性連絡人</span><span class="sxs-lookup"><span data-stu-id="2f720-103">Gets security contacts that were configured on this subscription</span></span>

## <span data-ttu-id="2f720-104">語法</span><span class="sxs-lookup"><span data-stu-id="2f720-104">SYNTAX</span></span>

### <span data-ttu-id="2f720-105">SubscriptionScope (預設) </span><span class="sxs-lookup"><span data-stu-id="2f720-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityContact [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f720-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="2f720-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityContact -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f720-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f720-107">ResourceId</span></span>
```
Get-AzSecurityContact -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f720-108">描述</span><span class="sxs-lookup"><span data-stu-id="2f720-108">DESCRIPTION</span></span>
<span data-ttu-id="2f720-109">獲得此訂閱上所配置的安全性連絡人。</span><span class="sxs-lookup"><span data-stu-id="2f720-109">Gets security contacts that were configured on this subscription.</span></span>
<span data-ttu-id="2f720-110">安全性連絡人可以取得訂閱上的安全性警示通知。</span><span class="sxs-lookup"><span data-stu-id="2f720-110">The security contact can get notifications on security alerts that happen on the subscription.</span></span>

## <span data-ttu-id="2f720-111">例子</span><span class="sxs-lookup"><span data-stu-id="2f720-111">EXAMPLES</span></span>

### <span data-ttu-id="2f720-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="2f720-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityContact
Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/default1
Name               : default1
Email              : ascasc@microsoft.com
Phone              : 123123123
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="2f720-113">在訂閱上獲得所有已配置的安全性連絡人</span><span class="sxs-lookup"><span data-stu-id="2f720-113">Gets all the configured security contacts on the subscription</span></span>

## <span data-ttu-id="2f720-114">參數</span><span class="sxs-lookup"><span data-stu-id="2f720-114">PARAMETERS</span></span>

### <span data-ttu-id="2f720-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f720-115">-DefaultProfile</span></span>
<span data-ttu-id="2f720-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2f720-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f720-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="2f720-117">-Name</span></span>
<span data-ttu-id="2f720-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="2f720-118">Resource name.</span></span>

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

### <span data-ttu-id="2f720-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f720-119">-ResourceId</span></span>
<span data-ttu-id="2f720-120">資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f720-120">Resource ID.</span></span>

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

### <span data-ttu-id="2f720-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f720-121">CommonParameters</span></span>
<span data-ttu-id="2f720-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2f720-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f720-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f720-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f720-124">輸入</span><span class="sxs-lookup"><span data-stu-id="2f720-124">INPUTS</span></span>

### <span data-ttu-id="2f720-125">System.String</span><span class="sxs-lookup"><span data-stu-id="2f720-125">System.String</span></span>

## <span data-ttu-id="2f720-126">輸出</span><span class="sxs-lookup"><span data-stu-id="2f720-126">OUTPUTS</span></span>

### <span data-ttu-id="2f720-127">Microsoft.Azure.Commands.Security.models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="2f720-127">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="2f720-128">筆記</span><span class="sxs-lookup"><span data-stu-id="2f720-128">NOTES</span></span>

## <span data-ttu-id="2f720-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="2f720-129">RELATED LINKS</span></span>
