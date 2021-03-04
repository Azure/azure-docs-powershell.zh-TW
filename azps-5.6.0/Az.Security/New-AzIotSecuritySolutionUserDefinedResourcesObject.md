---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzIotSecuritySolutionUserDefinedResourcesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
ms.openlocfilehash: 2b524234b18e84247c3789119fbfe1d214514fec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909958"
---
# <span data-ttu-id="52b05-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span><span class="sxs-lookup"><span data-stu-id="52b05-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span></span>

## <span data-ttu-id="52b05-102">簡介</span><span class="sxs-lookup"><span data-stu-id="52b05-102">SYNOPSIS</span></span>
<span data-ttu-id="52b05-103">建立 iot 安全性解決方案的新使用者定義資源</span><span class="sxs-lookup"><span data-stu-id="52b05-103">Create new user defined resources for iot security solution</span></span>

## <span data-ttu-id="52b05-104">語法</span><span class="sxs-lookup"><span data-stu-id="52b05-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionUserDefinedResourcesObject -Query <String> -QuerySubscriptionList <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52b05-105">描述</span><span class="sxs-lookup"><span data-stu-id="52b05-105">DESCRIPTION</span></span>
<span data-ttu-id="52b05-106">AzIotSecuritySolutionUserDefinedResourcesObject Cmdlet 會為 iot 安全性解決方案建立一個新的使用者定義資源物件。</span><span class="sxs-lookup"><span data-stu-id="52b05-106">The AzIotSecuritySolutionUserDefinedResourcesObject cmdlet creates a new user defined resources object for the iot security solution.</span></span>

## <span data-ttu-id="52b05-107">例子</span><span class="sxs-lookup"><span data-stu-id="52b05-107">EXAMPLES</span></span>

### <span data-ttu-id="52b05-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="52b05-108">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")

Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
QuerySubscriptions: ["XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX"]
```

<span data-ttu-id="52b05-109">建立新使用者定義資源</span><span class="sxs-lookup"><span data-stu-id="52b05-109">Create new user defined resources</span></span>

## <span data-ttu-id="52b05-110">參數</span><span class="sxs-lookup"><span data-stu-id="52b05-110">PARAMETERS</span></span>

### <span data-ttu-id="52b05-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b05-111">-DefaultProfile</span></span>
<span data-ttu-id="52b05-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="52b05-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52b05-113">-查詢</span><span class="sxs-lookup"><span data-stu-id="52b05-113">-Query</span></span>
<span data-ttu-id="52b05-114">查詢。</span><span class="sxs-lookup"><span data-stu-id="52b05-114">Query.</span></span>

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

### <span data-ttu-id="52b05-115">-QuerySubscriptionList</span><span class="sxs-lookup"><span data-stu-id="52b05-115">-QuerySubscriptionList</span></span>
<span data-ttu-id="52b05-116">查詢訂閱。</span><span class="sxs-lookup"><span data-stu-id="52b05-116">Query subscriptions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b05-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b05-117">CommonParameters</span></span>
<span data-ttu-id="52b05-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="52b05-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b05-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52b05-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b05-120">輸入</span><span class="sxs-lookup"><span data-stu-id="52b05-120">INPUTS</span></span>

### <span data-ttu-id="52b05-121">沒有</span><span class="sxs-lookup"><span data-stu-id="52b05-121">None</span></span>

## <span data-ttu-id="52b05-122">輸出</span><span class="sxs-lookup"><span data-stu-id="52b05-122">OUTPUTS</span></span>

### <span data-ttu-id="52b05-123">Microsoft.Azure.Commands.Security.models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="52b05-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

## <span data-ttu-id="52b05-124">筆記</span><span class="sxs-lookup"><span data-stu-id="52b05-124">NOTES</span></span>

## <span data-ttu-id="52b05-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="52b05-125">RELATED LINKS</span></span>
