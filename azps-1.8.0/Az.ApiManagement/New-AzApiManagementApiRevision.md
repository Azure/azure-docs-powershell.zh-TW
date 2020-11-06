---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRevision.md
ms.openlocfilehash: 81a80acdfb89f30cc1add6b1cfc10bcd7d745dfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611588"
---
# <span data-ttu-id="6f1eb-101">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6f1eb-101">New-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="6f1eb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6f1eb-102">SYNOPSIS</span></span>
<span data-ttu-id="6f1eb-103">建立現有 API 的新修訂版本。</span><span class="sxs-lookup"><span data-stu-id="6f1eb-103">Creates a new Revision of an Existing API.</span></span>

## <span data-ttu-id="6f1eb-104">句法</span><span class="sxs-lookup"><span data-stu-id="6f1eb-104">SYNTAX</span></span>

```
New-AzApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f1eb-105">說明</span><span class="sxs-lookup"><span data-stu-id="6f1eb-105">DESCRIPTION</span></span>

<span data-ttu-id="6f1eb-106">**AzApiManagementApiRevision** Cmdlet 會在 api 管理內容中為現有 API 建立 api 修正。</span><span class="sxs-lookup"><span data-stu-id="6f1eb-106">The **New-AzApiManagementApiRevision** cmdlet creates an API Revision for an existing an API in API Management context.</span></span>

## <span data-ttu-id="6f1eb-107">示例</span><span class="sxs-lookup"><span data-stu-id="6f1eb-107">EXAMPLES</span></span>

### <span data-ttu-id="6f1eb-108">範例1：建立 API 的 API 修訂</span><span class="sxs-lookup"><span data-stu-id="6f1eb-108">Example 1: Create an API Revision for an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRevision -Context $ApiMgmtContext  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6


ApiId                         : 5adf6fbf0faadf3ad8558065;rev=6
Name                          : httpbin.org
Description                   : API Management facade for a very handy and free online HTTP tool.
ServiceUrl                    : https://httpbin.org/
Path                          : httpbin
ApiType                       : http
Protocols                     : {Http, Https}
AuthorizationServerId         : contoso-oauth
AuthorizationScope            : contoso-oauth
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 6
ApiVersion                    : v1
IsCurrent                     : False
IsOnline                      : False
Id                            : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065;rev=6
ResourceGroupName             : Api-Default-WestUS
ServiceName                   : contoso
```

<span data-ttu-id="6f1eb-109">這個命令會建立 api 的 API 版本 `2` `echo-api` 。</span><span class="sxs-lookup"><span data-stu-id="6f1eb-109">This command creates an API Revision `2` of the `echo-api` API.</span></span>

## <span data-ttu-id="6f1eb-110">參數</span><span class="sxs-lookup"><span data-stu-id="6f1eb-110">PARAMETERS</span></span>

### <span data-ttu-id="6f1eb-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6f1eb-111">-ApiId</span></span>
<span data-ttu-id="6f1eb-112">要建立其修正的 API 識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f1eb-112">Identifier for API whose Revision is to be created.</span></span>

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

### <span data-ttu-id="6f1eb-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="6f1eb-113">-ApiRevision</span></span>
<span data-ttu-id="6f1eb-114">Api 的修訂識別碼。</span><span class="sxs-lookup"><span data-stu-id="6f1eb-114">Revision Identifier of the Api.</span></span>

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

### <span data-ttu-id="6f1eb-115">-內容</span><span class="sxs-lookup"><span data-stu-id="6f1eb-115">-Context</span></span>
<span data-ttu-id="6f1eb-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="6f1eb-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6f1eb-117">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="6f1eb-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f1eb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f1eb-118">-DefaultProfile</span></span>
<span data-ttu-id="6f1eb-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f1eb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f1eb-120">-確認</span><span class="sxs-lookup"><span data-stu-id="6f1eb-120">-Confirm</span></span>
<span data-ttu-id="6f1eb-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6f1eb-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f1eb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f1eb-122">-WhatIf</span></span>
<span data-ttu-id="6f1eb-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f1eb-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f1eb-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f1eb-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f1eb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f1eb-125">CommonParameters</span></span>
<span data-ttu-id="6f1eb-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6f1eb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f1eb-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6f1eb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f1eb-128">輸入</span><span class="sxs-lookup"><span data-stu-id="6f1eb-128">INPUTS</span></span>

### <span data-ttu-id="6f1eb-129">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="6f1eb-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6f1eb-130">System.object</span><span class="sxs-lookup"><span data-stu-id="6f1eb-130">System.String</span></span>

## <span data-ttu-id="6f1eb-131">輸出</span><span class="sxs-lookup"><span data-stu-id="6f1eb-131">OUTPUTS</span></span>

### <span data-ttu-id="6f1eb-132">ServiceManagement. PsApiManagementApi （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="6f1eb-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="6f1eb-133">筆記</span><span class="sxs-lookup"><span data-stu-id="6f1eb-133">NOTES</span></span>

## <span data-ttu-id="6f1eb-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f1eb-134">RELATED LINKS</span></span>

[<span data-ttu-id="6f1eb-135">AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f1eb-135">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="6f1eb-136">移除-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f1eb-136">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="6f1eb-137">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6f1eb-137">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)
