---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementApiRevision.md
ms.openlocfilehash: 16c108d4f62d9bcc44176fce7ede9a7e56d98687
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447639"
---
# <span data-ttu-id="ffdfa-101">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="ffdfa-101">Get-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="ffdfa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ffdfa-102">SYNOPSIS</span></span>
<span data-ttu-id="ffdfa-103">取得 API 所有 API 修訂的詳細資料</span><span class="sxs-lookup"><span data-stu-id="ffdfa-103">Gets details of all the API Revisions of an API</span></span>

## <span data-ttu-id="ffdfa-104">句法</span><span class="sxs-lookup"><span data-stu-id="ffdfa-104">SYNTAX</span></span>

```
Get-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffdfa-105">說明</span><span class="sxs-lookup"><span data-stu-id="ffdfa-105">DESCRIPTION</span></span>
<span data-ttu-id="ffdfa-106">**AzApiManagementApiRevision** Cmdlet 會取得 API 所有修訂的詳細資料</span><span class="sxs-lookup"><span data-stu-id="ffdfa-106">The **Get-AzApiManagementApiRevision** cmdlet gets the details of all revisions of an API</span></span>

## <span data-ttu-id="ffdfa-107">示例</span><span class="sxs-lookup"><span data-stu-id="ffdfa-107">EXAMPLES</span></span>

### <span data-ttu-id="ffdfa-108">範例1：取得 API 的所有 API 修訂</span><span class="sxs-lookup"><span data-stu-id="ffdfa-108">Example 1: Get all API Revisions of an API</span></span>
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

<span data-ttu-id="ffdfa-109">這個命令會針對特定的 ApiManagement 內容，取得指定 API 的所有 API 修正。</span><span class="sxs-lookup"><span data-stu-id="ffdfa-109">This command gets all of the API revision of specified API for particular ApiManagement Context.</span></span>

## <span data-ttu-id="ffdfa-110">參數</span><span class="sxs-lookup"><span data-stu-id="ffdfa-110">PARAMETERS</span></span>

### <span data-ttu-id="ffdfa-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ffdfa-111">-ApiId</span></span>
<span data-ttu-id="ffdfa-112">我們想要清單修改的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="ffdfa-112">API identifier whose revisions we want to list.</span></span>
<span data-ttu-id="ffdfa-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="ffdfa-113">This parameter is required.</span></span>

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

### <span data-ttu-id="ffdfa-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="ffdfa-114">-ApiRevision</span></span>
<span data-ttu-id="ffdfa-115">特定 Api 修訂的修訂識別碼。</span><span class="sxs-lookup"><span data-stu-id="ffdfa-115">Revision Identifier of the particular Api revision.</span></span> <span data-ttu-id="ffdfa-116">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="ffdfa-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="ffdfa-117">-內容</span><span class="sxs-lookup"><span data-stu-id="ffdfa-117">-Context</span></span>
<span data-ttu-id="ffdfa-118">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="ffdfa-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ffdfa-119">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="ffdfa-119">This parameter is required.</span></span>

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

### <span data-ttu-id="ffdfa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffdfa-120">-DefaultProfile</span></span>
<span data-ttu-id="ffdfa-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ffdfa-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffdfa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffdfa-122">CommonParameters</span></span>
<span data-ttu-id="ffdfa-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ffdfa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffdfa-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ffdfa-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffdfa-125">輸入</span><span class="sxs-lookup"><span data-stu-id="ffdfa-125">INPUTS</span></span>

### <span data-ttu-id="ffdfa-126">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="ffdfa-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ffdfa-127">System.object</span><span class="sxs-lookup"><span data-stu-id="ffdfa-127">System.String</span></span>

## <span data-ttu-id="ffdfa-128">輸出</span><span class="sxs-lookup"><span data-stu-id="ffdfa-128">OUTPUTS</span></span>

### <span data-ttu-id="ffdfa-129">ServiceManagement. PsApiManagementApiRevision （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="ffdfa-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRevision</span></span>

## <span data-ttu-id="ffdfa-130">筆記</span><span class="sxs-lookup"><span data-stu-id="ffdfa-130">NOTES</span></span>

## <span data-ttu-id="ffdfa-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="ffdfa-131">RELATED LINKS</span></span>
