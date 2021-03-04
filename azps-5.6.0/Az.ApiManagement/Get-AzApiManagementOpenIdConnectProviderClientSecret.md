---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: 0c6757b32a81c689b4b9bbc3397fdd52c19ae4bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917513"
---
# <span data-ttu-id="4dcc5-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="4dcc5-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="4dcc5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4dcc5-102">SYNOPSIS</span></span>
<span data-ttu-id="4dcc5-103">獲得 OpenID Connect 提供者用戶端金鑰。</span><span class="sxs-lookup"><span data-stu-id="4dcc5-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="4dcc5-104">語法</span><span class="sxs-lookup"><span data-stu-id="4dcc5-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4dcc5-105">描述</span><span class="sxs-lookup"><span data-stu-id="4dcc5-105">DESCRIPTION</span></span>
<span data-ttu-id="4dcc5-106">獲得 OpenID Connect 提供者用戶端金鑰。</span><span class="sxs-lookup"><span data-stu-id="4dcc5-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="4dcc5-107">例子</span><span class="sxs-lookup"><span data-stu-id="4dcc5-107">EXAMPLES</span></span>

### <span data-ttu-id="4dcc5-108">範例 1：使用識別碼取得提供者用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="4dcc5-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="4dcc5-109">此命令會獲得具有識別碼為 ISPPROvider01 之提供者的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="4dcc5-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="4dcc5-110">參數</span><span class="sxs-lookup"><span data-stu-id="4dcc5-110">PARAMETERS</span></span>

### <span data-ttu-id="4dcc5-111">-內容</span><span class="sxs-lookup"><span data-stu-id="4dcc5-111">-Context</span></span>
<span data-ttu-id="4dcc5-112">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="4dcc5-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4dcc5-113">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="4dcc5-113">This parameter is required.</span></span>

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

### <span data-ttu-id="4dcc5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dcc5-114">-DefaultProfile</span></span>
<span data-ttu-id="4dcc5-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4dcc5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dcc5-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="4dcc5-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="4dcc5-117">OpenID Connect 提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4dcc5-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="4dcc5-118">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="4dcc5-118">This parameter is required.</span></span>

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

### <span data-ttu-id="4dcc5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dcc5-119">CommonParameters</span></span>
<span data-ttu-id="4dcc5-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4dcc5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dcc5-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4dcc5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dcc5-122">輸入</span><span class="sxs-lookup"><span data-stu-id="4dcc5-122">INPUTS</span></span>

### <span data-ttu-id="4dcc5-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="4dcc5-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4dcc5-124">System.String</span><span class="sxs-lookup"><span data-stu-id="4dcc5-124">System.String</span></span>

## <span data-ttu-id="4dcc5-125">輸出</span><span class="sxs-lookup"><span data-stu-id="4dcc5-125">OUTPUTS</span></span>

### <span data-ttu-id="4dcc5-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="4dcc5-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="4dcc5-127">筆記</span><span class="sxs-lookup"><span data-stu-id="4dcc5-127">NOTES</span></span>

## <span data-ttu-id="4dcc5-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="4dcc5-128">RELATED LINKS</span></span>
