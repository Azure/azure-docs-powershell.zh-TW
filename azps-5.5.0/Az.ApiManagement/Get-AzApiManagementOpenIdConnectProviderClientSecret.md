---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProviderClientSecret.md
ms.openlocfilehash: dcc66b6d28157ff9d5551e2fdf0cab18f7727828
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139674"
---
# <span data-ttu-id="a9f93-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="a9f93-101">Get-AzApiManagementOpenIdConnectProviderClientSecret</span></span>

## <span data-ttu-id="a9f93-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9f93-102">SYNOPSIS</span></span>
<span data-ttu-id="a9f93-103">取得 OpenID Connect provider 用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="a9f93-103">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="a9f93-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9f93-104">SYNTAX</span></span>

```
Get-AzApiManagementOpenIdConnectProviderClientSecret -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9f93-105">說明</span><span class="sxs-lookup"><span data-stu-id="a9f93-105">DESCRIPTION</span></span>
<span data-ttu-id="a9f93-106">取得 OpenID Connect provider 用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="a9f93-106">Gets OpenID Connect provider client secret.</span></span>

## <span data-ttu-id="a9f93-107">示例</span><span class="sxs-lookup"><span data-stu-id="a9f93-107">EXAMPLES</span></span>

### <span data-ttu-id="a9f93-108">範例1：使用 ID 取得提供者用戶端密碼</span><span class="sxs-lookup"><span data-stu-id="a9f93-108">Example 1: Get a provider client secret by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProviderClientSecret -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="a9f93-109">這個命令會取得具有識別碼 OICProvider01 之提供者的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="a9f93-109">This command gets a client secret of the provider that has the ID OICProvider01.</span></span>

## <span data-ttu-id="a9f93-110">參數</span><span class="sxs-lookup"><span data-stu-id="a9f93-110">PARAMETERS</span></span>

### <span data-ttu-id="a9f93-111">-內容</span><span class="sxs-lookup"><span data-stu-id="a9f93-111">-Context</span></span>
<span data-ttu-id="a9f93-112">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="a9f93-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a9f93-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a9f93-113">This parameter is required.</span></span>

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

### <span data-ttu-id="a9f93-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9f93-114">-DefaultProfile</span></span>
<span data-ttu-id="a9f93-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9f93-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9f93-116">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="a9f93-116">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="a9f93-117">OpenID Connect 提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9f93-117">Identifier of a OpenID Connect Provider.</span></span>
<span data-ttu-id="a9f93-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a9f93-118">This parameter is required.</span></span>

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

### <span data-ttu-id="a9f93-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9f93-119">CommonParameters</span></span>
<span data-ttu-id="a9f93-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9f93-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9f93-121">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a9f93-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9f93-122">輸入</span><span class="sxs-lookup"><span data-stu-id="a9f93-122">INPUTS</span></span>

### <span data-ttu-id="a9f93-123">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a9f93-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a9f93-124">System.object</span><span class="sxs-lookup"><span data-stu-id="a9f93-124">System.String</span></span>

## <span data-ttu-id="a9f93-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a9f93-125">OUTPUTS</span></span>

### <span data-ttu-id="a9f93-126">ServiceManagement. PsApiManagementClientSecret （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a9f93-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="a9f93-127">筆記</span><span class="sxs-lookup"><span data-stu-id="a9f93-127">NOTES</span></span>

## <span data-ttu-id="a9f93-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9f93-128">RELATED LINKS</span></span>
