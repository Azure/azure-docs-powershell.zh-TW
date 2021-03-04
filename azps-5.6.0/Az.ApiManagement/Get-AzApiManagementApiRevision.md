---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
ms.openlocfilehash: e653053264baaa343b474f534f30915d725e5553
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911797"
---
# <span data-ttu-id="72b8c-101">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="72b8c-101">Get-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="72b8c-102">簡介</span><span class="sxs-lookup"><span data-stu-id="72b8c-102">SYNOPSIS</span></span>
<span data-ttu-id="72b8c-103">獲得 API 所有 API 修訂的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="72b8c-103">Gets details of all the API Revisions of an API</span></span>

## <span data-ttu-id="72b8c-104">語法</span><span class="sxs-lookup"><span data-stu-id="72b8c-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72b8c-105">描述</span><span class="sxs-lookup"><span data-stu-id="72b8c-105">DESCRIPTION</span></span>
<span data-ttu-id="72b8c-106">**Get-AzApiManagementApiRevision Cmdlet** 會取得 API 所有修訂的詳細資訊</span><span class="sxs-lookup"><span data-stu-id="72b8c-106">The **Get-AzApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="72b8c-107">例子</span><span class="sxs-lookup"><span data-stu-id="72b8c-107">EXAMPLES</span></span>

### <span data-ttu-id="72b8c-108">範例 1：取得 API 的所有 API 修訂</span><span class="sxs-lookup"><span data-stu-id="72b8c-108">Example 1: Get all API Revisions of an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "5adf6fbf0faadf3ad8558065"

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=3
ApiRevision     : 3
CreatedDateTime : 4/26/2018 10:57:42 PM
UpdatedDateTime : 4/26/2018 10:57:42 PM
Description     : ddsds
PrivateUrl      : /httpbin/v1;rev=3
IsOnline        : True
IsCurrent       : False

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=2
ApiRevision     : 2
CreatedDateTime : 4/26/2018 10:57:33 PM
UpdatedDateTime : 4/26/2018 10:57:33 PM
Description     : AA
PrivateUrl      : /httpbin/v1
IsOnline        : True
IsCurrent       : True

ApiId           : /apis/5adf6fbf0faadf3ad8558065;rev=1
ApiRevision     : 1
CreatedDateTime : 4/24/2018 5:56:17 PM
UpdatedDateTime : 5/9/2018 9:29:06 PM
Description     :
PrivateUrl      : /httpbin/v1;rev=1
IsOnline        : True
IsCurrent       : False
```

<span data-ttu-id="72b8c-109">此命令會針對特定 ApiManagement 上下文，獲得指定 API 的所有 API 修訂。</span><span class="sxs-lookup"><span data-stu-id="72b8c-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="72b8c-110">參數</span><span class="sxs-lookup"><span data-stu-id="72b8c-110">PARAMETERS</span></span>

### <span data-ttu-id="72b8c-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="72b8c-111">-ApiId</span></span>
<span data-ttu-id="72b8c-112">我們要列出修訂的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="72b8c-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="72b8c-113">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="72b8c-113">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72b8c-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="72b8c-114">-ApiRevision</span></span>
<span data-ttu-id="72b8c-115">特定 Api 修訂的修訂識別碼。</span><span class="sxs-lookup"><span data-stu-id="72b8c-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="72b8c-116">此參數為選擇性。</span><span class="sxs-lookup"><span data-stu-id="72b8c-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="72b8c-117">-內容</span><span class="sxs-lookup"><span data-stu-id="72b8c-117">-Context</span></span>
<span data-ttu-id="72b8c-118">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="72b8c-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="72b8c-119">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="72b8c-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72b8c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72b8c-120">-DefaultProfile</span></span>
<span data-ttu-id="72b8c-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="72b8c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72b8c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72b8c-122">CommonParameters</span></span>
<span data-ttu-id="72b8c-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="72b8c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72b8c-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72b8c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72b8c-125">輸入</span><span class="sxs-lookup"><span data-stu-id="72b8c-125">INPUTS</span></span>

### <span data-ttu-id="72b8c-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="72b8c-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="72b8c-127">System.String</span><span class="sxs-lookup"><span data-stu-id="72b8c-127">System.String</span></span>

## <span data-ttu-id="72b8c-128">輸出</span><span class="sxs-lookup"><span data-stu-id="72b8c-128">OUTPUTS</span></span>

### <span data-ttu-id="72b8c-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="72b8c-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="72b8c-130">筆記</span><span class="sxs-lookup"><span data-stu-id="72b8c-130">NOTES</span></span>

## <span data-ttu-id="72b8c-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="72b8c-131">RELATED LINKS</span></span>
