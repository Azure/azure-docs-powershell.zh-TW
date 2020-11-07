---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 94e7889d1c59d7e132d10e8da6881dc88e612287
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957886"
---
# <span data-ttu-id="9485d-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="9485d-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="9485d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9485d-102">SYNOPSIS</span></span>
<span data-ttu-id="9485d-103">取得 API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="9485d-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="9485d-104">句法</span><span class="sxs-lookup"><span data-stu-id="9485d-104">SYNTAX</span></span>

### <span data-ttu-id="9485d-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9485d-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9485d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9485d-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9485d-107">說明</span><span class="sxs-lookup"><span data-stu-id="9485d-107">DESCRIPTION</span></span>
<span data-ttu-id="9485d-108">**AzApiManagementAuthorizationServer** Cmdlet 會取得所有 Azure API 管理授權伺服器或指定的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="9485d-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="9485d-109">示例</span><span class="sxs-lookup"><span data-stu-id="9485d-109">EXAMPLES</span></span>

### <span data-ttu-id="9485d-110">範例1：取得所有授權伺服器</span><span class="sxs-lookup"><span data-stu-id="9485d-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="9485d-111">這個命令會取得所有 API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="9485d-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="9485d-112">範例2：取得指定的授權伺服器</span><span class="sxs-lookup"><span data-stu-id="9485d-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="9485d-113">這個命令會取得指定的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="9485d-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="9485d-114">參數</span><span class="sxs-lookup"><span data-stu-id="9485d-114">PARAMETERS</span></span>

### <span data-ttu-id="9485d-115">-內容</span><span class="sxs-lookup"><span data-stu-id="9485d-115">-Context</span></span>

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

### <span data-ttu-id="9485d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9485d-116">-DefaultProfile</span></span>
<span data-ttu-id="9485d-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9485d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9485d-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9485d-118">-ResourceId</span></span>
<span data-ttu-id="9485d-119">授權伺服器的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9485d-119">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="9485d-120">如果已指定，將會嘗試依據識別碼尋找授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="9485d-120">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="9485d-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="9485d-121">This parameter is required.</span></span>

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

### <span data-ttu-id="9485d-122">-ServerId</span><span class="sxs-lookup"><span data-stu-id="9485d-122">-ServerId</span></span>
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

### <span data-ttu-id="9485d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9485d-123">CommonParameters</span></span>
<span data-ttu-id="9485d-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9485d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9485d-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9485d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9485d-126">輸入</span><span class="sxs-lookup"><span data-stu-id="9485d-126">INPUTS</span></span>

### <span data-ttu-id="9485d-127">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="9485d-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9485d-128">System.object</span><span class="sxs-lookup"><span data-stu-id="9485d-128">System.String</span></span>

## <span data-ttu-id="9485d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="9485d-129">OUTPUTS</span></span>

### <span data-ttu-id="9485d-130">ServiceManagement. PsApiManagementOAuth2AuthorizationServer （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="9485d-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="9485d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="9485d-131">NOTES</span></span>

## <span data-ttu-id="9485d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="9485d-132">RELATED LINKS</span></span>

[<span data-ttu-id="9485d-133">新-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="9485d-133">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="9485d-134">移除-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="9485d-134">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="9485d-135">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="9485d-135">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


