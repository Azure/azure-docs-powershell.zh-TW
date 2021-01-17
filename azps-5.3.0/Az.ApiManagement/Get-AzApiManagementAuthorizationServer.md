---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ad06e1f9c37920c2362db3a94cdfbace91bf3796
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98447631"
---
# <span data-ttu-id="329e1-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="329e1-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="329e1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="329e1-102">SYNOPSIS</span></span>
<span data-ttu-id="329e1-103">取得 API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="329e1-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="329e1-104">句法</span><span class="sxs-lookup"><span data-stu-id="329e1-104">SYNTAX</span></span>

### <span data-ttu-id="329e1-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="329e1-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="329e1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="329e1-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="329e1-107">說明</span><span class="sxs-lookup"><span data-stu-id="329e1-107">DESCRIPTION</span></span>
<span data-ttu-id="329e1-108">**AzApiManagementAuthorizationServer** Cmdlet 會取得所有 Azure API 管理授權伺服器或指定的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="329e1-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization server.</span></span>
<span data-ttu-id="329e1-109">ClientSecret 不會包含在結果詳細資料中。</span><span class="sxs-lookup"><span data-stu-id="329e1-109">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="329e1-110">若要取得用戶端密碼，請使用 **AzApiManagementAuthorizationServerClientSecret**。</span><span class="sxs-lookup"><span data-stu-id="329e1-110">To get client secret, use **Get-AzApiManagementAuthorizationServerClientSecret**.</span></span>

## <span data-ttu-id="329e1-111">示例</span><span class="sxs-lookup"><span data-stu-id="329e1-111">EXAMPLES</span></span>

### <span data-ttu-id="329e1-112">範例1：取得所有授權伺服器</span><span class="sxs-lookup"><span data-stu-id="329e1-112">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="329e1-113">這個命令會取得所有 API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="329e1-113">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="329e1-114">範例2：取得指定的授權伺服器</span><span class="sxs-lookup"><span data-stu-id="329e1-114">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="329e1-115">這個命令會取得指定的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="329e1-115">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="329e1-116">參數</span><span class="sxs-lookup"><span data-stu-id="329e1-116">PARAMETERS</span></span>

### <span data-ttu-id="329e1-117">-內容</span><span class="sxs-lookup"><span data-stu-id="329e1-117">-Context</span></span>

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

### <span data-ttu-id="329e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="329e1-118">-DefaultProfile</span></span>
<span data-ttu-id="329e1-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="329e1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="329e1-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="329e1-120">-ResourceId</span></span>
<span data-ttu-id="329e1-121">授權伺服器的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="329e1-121">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="329e1-122">如果已指定，將會嘗試依據識別碼尋找授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="329e1-122">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="329e1-123">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="329e1-123">This parameter is required.</span></span>

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

### <span data-ttu-id="329e1-124">-ServerId</span><span class="sxs-lookup"><span data-stu-id="329e1-124">-ServerId</span></span>
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

### <span data-ttu-id="329e1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="329e1-125">CommonParameters</span></span>
<span data-ttu-id="329e1-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="329e1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="329e1-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="329e1-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="329e1-128">輸入</span><span class="sxs-lookup"><span data-stu-id="329e1-128">INPUTS</span></span>

### <span data-ttu-id="329e1-129">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="329e1-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="329e1-130">System.object</span><span class="sxs-lookup"><span data-stu-id="329e1-130">System.String</span></span>

## <span data-ttu-id="329e1-131">輸出</span><span class="sxs-lookup"><span data-stu-id="329e1-131">OUTPUTS</span></span>

### <span data-ttu-id="329e1-132">ServiceManagement. PsApiManagementOAuth2AuthorizationServer （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="329e1-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="329e1-133">筆記</span><span class="sxs-lookup"><span data-stu-id="329e1-133">NOTES</span></span>

## <span data-ttu-id="329e1-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="329e1-134">RELATED LINKS</span></span>

[<span data-ttu-id="329e1-135">新-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="329e1-135">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="329e1-136">移除-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="329e1-136">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="329e1-137">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="329e1-137">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


