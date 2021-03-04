---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 098fb692e1710b9463650f0e398d999f0a2b1062
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909865"
---
# <span data-ttu-id="b06c4-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b06c4-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="b06c4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b06c4-102">SYNOPSIS</span></span>
<span data-ttu-id="b06c4-103">獲得 API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="b06c4-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="b06c4-104">語法</span><span class="sxs-lookup"><span data-stu-id="b06c4-104">SYNTAX</span></span>

### <span data-ttu-id="b06c4-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b06c4-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b06c4-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b06c4-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b06c4-107">描述</span><span class="sxs-lookup"><span data-stu-id="b06c4-107">DESCRIPTION</span></span>
<span data-ttu-id="b06c4-108">**Get-AzApiManagementAuthorizationServer** Cmdlet 會取得所有 Azure API 管理授權伺服器或指定的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="b06c4-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization server.</span></span>
<span data-ttu-id="b06c4-109">ClientSecret 不會包含在結果詳細資料中。</span><span class="sxs-lookup"><span data-stu-id="b06c4-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="b06c4-110">若要取得用戶端密碼，請使用 **Get-AzApiManagementAuthorizationServerClientSecret。**</span><span class="sxs-lookup"><span data-stu-id="b06c4-110">To get client secret, use **Get-AzApiManagementAuthorizationServerClientSecret**.</span></span>

## <span data-ttu-id="b06c4-111">例子</span><span class="sxs-lookup"><span data-stu-id="b06c4-111">EXAMPLES</span></span>

### <span data-ttu-id="b06c4-112">範例 1：取得所有授權伺服器</span><span class="sxs-lookup"><span data-stu-id="b06c4-112">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="b06c4-113">此命令會獲得所有 API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="b06c4-113">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="b06c4-114">範例 2：取得指定的授權伺服器</span><span class="sxs-lookup"><span data-stu-id="b06c4-114">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="b06c4-115">此命令會獲得指定的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="b06c4-115">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="b06c4-116">參數</span><span class="sxs-lookup"><span data-stu-id="b06c4-116">PARAMETERS</span></span>

### <span data-ttu-id="b06c4-117">-內容</span><span class="sxs-lookup"><span data-stu-id="b06c4-117">-Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b06c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b06c4-118">-DefaultProfile</span></span>
<span data-ttu-id="b06c4-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b06c4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b06c4-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b06c4-120">-ResourceId</span></span>
<span data-ttu-id="b06c4-121">授權伺服器的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b06c4-121">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="b06c4-122">如果指定，會嘗試根據識別碼尋找授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="b06c4-122">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="b06c4-123">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="b06c4-123">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b06c4-124">-ServerId</span><span class="sxs-lookup"><span data-stu-id="b06c4-124">-ServerId</span></span>
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

### <span data-ttu-id="b06c4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b06c4-125">CommonParameters</span></span>
<span data-ttu-id="b06c4-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b06c4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b06c4-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b06c4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b06c4-128">輸入</span><span class="sxs-lookup"><span data-stu-id="b06c4-128">INPUTS</span></span>

### <span data-ttu-id="b06c4-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="b06c4-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b06c4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b06c4-130">System.String</span></span>

## <span data-ttu-id="b06c4-131">輸出</span><span class="sxs-lookup"><span data-stu-id="b06c4-131">OUTPUTS</span></span>

### <span data-ttu-id="b06c4-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementOAuth2AuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b06c4-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="b06c4-133">筆記</span><span class="sxs-lookup"><span data-stu-id="b06c4-133">NOTES</span></span>

## <span data-ttu-id="b06c4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="b06c4-134">RELATED LINKS</span></span>

[<span data-ttu-id="b06c4-135">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b06c4-135">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="b06c4-136">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b06c4-136">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="b06c4-137">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="b06c4-137">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


