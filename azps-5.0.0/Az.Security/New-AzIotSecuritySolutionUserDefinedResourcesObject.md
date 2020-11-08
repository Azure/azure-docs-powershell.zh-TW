---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionUserDefinedResourcesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
ms.openlocfilehash: e824c32ae2ae4f28972cdac9446eeeae6e410c75
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141251"
---
# <span data-ttu-id="000da-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span><span class="sxs-lookup"><span data-stu-id="000da-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span></span>

## <span data-ttu-id="000da-102">摘要</span><span class="sxs-lookup"><span data-stu-id="000da-102">SYNOPSIS</span></span>
<span data-ttu-id="000da-103">為 iot 安全解決方案建立新的使用者定義資源</span><span class="sxs-lookup"><span data-stu-id="000da-103">Create new user defined resources for iot security solution</span></span>

## <span data-ttu-id="000da-104">句法</span><span class="sxs-lookup"><span data-stu-id="000da-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionUserDefinedResourcesObject -Query <String> -QuerySubscriptionList <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="000da-105">說明</span><span class="sxs-lookup"><span data-stu-id="000da-105">DESCRIPTION</span></span>
<span data-ttu-id="000da-106">AzIotSecuritySolutionUserDefinedResourcesObject Cmdlet 會為 iot 安全解決方案建立新的使用者定義資源物件。</span><span class="sxs-lookup"><span data-stu-id="000da-106">The AzIotSecuritySolutionUserDefinedResourcesObject cmdlet creates a new user defined resources object for the iot security solution.</span></span>

## <span data-ttu-id="000da-107">示例</span><span class="sxs-lookup"><span data-stu-id="000da-107">EXAMPLES</span></span>

### <span data-ttu-id="000da-108">範例1</span><span class="sxs-lookup"><span data-stu-id="000da-108">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")

Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
QuerySubscriptions: ["XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX"]
```

<span data-ttu-id="000da-109">建立新的使用者定義資源</span><span class="sxs-lookup"><span data-stu-id="000da-109">Create new user defined resources</span></span>

## <span data-ttu-id="000da-110">參數</span><span class="sxs-lookup"><span data-stu-id="000da-110">PARAMETERS</span></span>

### <span data-ttu-id="000da-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="000da-111">-DefaultProfile</span></span>
<span data-ttu-id="000da-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="000da-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="000da-113">-Query</span><span class="sxs-lookup"><span data-stu-id="000da-113">-Query</span></span>
<span data-ttu-id="000da-114">Query.</span><span class="sxs-lookup"><span data-stu-id="000da-114">Query.</span></span>

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

### <span data-ttu-id="000da-115">-QuerySubscriptionList</span><span class="sxs-lookup"><span data-stu-id="000da-115">-QuerySubscriptionList</span></span>
<span data-ttu-id="000da-116">查詢訂閱。</span><span class="sxs-lookup"><span data-stu-id="000da-116">Query subscriptions.</span></span>

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

### <span data-ttu-id="000da-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="000da-117">CommonParameters</span></span>
<span data-ttu-id="000da-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="000da-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="000da-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="000da-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="000da-120">輸入</span><span class="sxs-lookup"><span data-stu-id="000da-120">INPUTS</span></span>

### <span data-ttu-id="000da-121">所有</span><span class="sxs-lookup"><span data-stu-id="000da-121">None</span></span>

## <span data-ttu-id="000da-122">輸出</span><span class="sxs-lookup"><span data-stu-id="000da-122">OUTPUTS</span></span>

### <span data-ttu-id="000da-123">PSUserDefinedResources 中的 IotSecuritySolutions （Security..。</span><span class="sxs-lookup"><span data-stu-id="000da-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

## <span data-ttu-id="000da-124">筆記</span><span class="sxs-lookup"><span data-stu-id="000da-124">NOTES</span></span>

## <span data-ttu-id="000da-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="000da-125">RELATED LINKS</span></span>
