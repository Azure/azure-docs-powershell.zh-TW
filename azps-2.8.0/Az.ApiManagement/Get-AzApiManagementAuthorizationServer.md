---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: ce401334b03620ac565c5dd3b737b7a2982575e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614064"
---
# <span data-ttu-id="50e08-101">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="50e08-101">Get-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="50e08-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50e08-102">SYNOPSIS</span></span>
<span data-ttu-id="50e08-103">取得 API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="50e08-103">Gets an API Management authorization server.</span></span>

## <span data-ttu-id="50e08-104">句法</span><span class="sxs-lookup"><span data-stu-id="50e08-104">SYNTAX</span></span>

### <span data-ttu-id="50e08-105">CoNtextParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="50e08-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50e08-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="50e08-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementAuthorizationServer [-ServerId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50e08-107">說明</span><span class="sxs-lookup"><span data-stu-id="50e08-107">DESCRIPTION</span></span>
<span data-ttu-id="50e08-108">**AzApiManagementAuthorizationServer** Cmdlet 會取得所有 Azure API 管理授權伺服器或指定的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="50e08-108">The **Get-AzApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="50e08-109">示例</span><span class="sxs-lookup"><span data-stu-id="50e08-109">EXAMPLES</span></span>

### <span data-ttu-id="50e08-110">範例1：取得所有授權伺服器</span><span class="sxs-lookup"><span data-stu-id="50e08-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementAuthorizationServer -Context $ApiMgmtContext
```

<span data-ttu-id="50e08-111">這個命令會取得所有 API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="50e08-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="50e08-112">範例2：取得指定的授權伺服器</span><span class="sxs-lookup"><span data-stu-id="50e08-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="50e08-113">這個命令會取得指定的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="50e08-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="50e08-114">參數</span><span class="sxs-lookup"><span data-stu-id="50e08-114">PARAMETERS</span></span>

### <span data-ttu-id="50e08-115">-內容</span><span class="sxs-lookup"><span data-stu-id="50e08-115">-Context</span></span>

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

### <span data-ttu-id="50e08-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50e08-116">-DefaultProfile</span></span>
<span data-ttu-id="50e08-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="50e08-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50e08-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50e08-118">-ResourceId</span></span>
<span data-ttu-id="50e08-119">授權伺服器的 Arm 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="50e08-119">Arm Resource Identifier of the authorization server.</span></span> <span data-ttu-id="50e08-120">如果已指定，將會嘗試依據識別碼尋找授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="50e08-120">If specified will try to find authorization server by the identifier.</span></span> <span data-ttu-id="50e08-121">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="50e08-121">This parameter is required.</span></span>

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

### <span data-ttu-id="50e08-122">-ServerId</span><span class="sxs-lookup"><span data-stu-id="50e08-122">-ServerId</span></span>
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

### <span data-ttu-id="50e08-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50e08-123">CommonParameters</span></span>
<span data-ttu-id="50e08-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50e08-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50e08-125">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="50e08-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50e08-126">輸入</span><span class="sxs-lookup"><span data-stu-id="50e08-126">INPUTS</span></span>

### <span data-ttu-id="50e08-127">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="50e08-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="50e08-128">System.object</span><span class="sxs-lookup"><span data-stu-id="50e08-128">System.String</span></span>

## <span data-ttu-id="50e08-129">輸出</span><span class="sxs-lookup"><span data-stu-id="50e08-129">OUTPUTS</span></span>

### <span data-ttu-id="50e08-130">ServiceManagement. PsApiManagementOAuth2AuthorizationServer （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="50e08-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthorizationServer</span></span>

## <span data-ttu-id="50e08-131">筆記</span><span class="sxs-lookup"><span data-stu-id="50e08-131">NOTES</span></span>

## <span data-ttu-id="50e08-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="50e08-132">RELATED LINKS</span></span>

[<span data-ttu-id="50e08-133">新-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="50e08-133">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="50e08-134">移除-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="50e08-134">Remove-AzApiManagementAuthorizationServer</span></span>](./Remove-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="50e08-135">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="50e08-135">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


