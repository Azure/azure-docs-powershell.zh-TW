---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementidentityproviderclientsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProviderClientSecret.md
ms.openlocfilehash: 94480eb224d9ef6cb4e4244fc863e79c39a8d23e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913625"
---
# <span data-ttu-id="c1c93-101">Get-AzApiManagementIdentityProviderClientSecret</span><span class="sxs-lookup"><span data-stu-id="c1c93-101">Get-AzApiManagementIdentityProviderClientSecret</span></span>

## <span data-ttu-id="c1c93-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c1c93-102">SYNOPSIS</span></span>
<span data-ttu-id="c1c93-103">取得身分識別提供者用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="c1c93-103">Get the identity provider client secret.</span></span>

## <span data-ttu-id="c1c93-104">語法</span><span class="sxs-lookup"><span data-stu-id="c1c93-104">SYNTAX</span></span>

```
Get-AzApiManagementIdentityProviderClientSecret -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1c93-105">描述</span><span class="sxs-lookup"><span data-stu-id="c1c93-105">DESCRIPTION</span></span>
<span data-ttu-id="c1c93-106">取得身分識別提供者用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="c1c93-106">Get the identity provider client secret.</span></span>

## <span data-ttu-id="c1c93-107">例子</span><span class="sxs-lookup"><span data-stu-id="c1c93-107">EXAMPLES</span></span>

### <span data-ttu-id="c1c93-108">範例 1：取得 AAD 類型身分識別提供者的用戶端機密</span><span class="sxs-lookup"><span data-stu-id="c1c93-108">Example 1: Get the client secret of AAD Type Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Get-AzApiManagementIdentityProviderClientSecret -Context $apimContext -Type Aad
```

<span data-ttu-id="c1c93-109">獲得 Azure Active Directory 身分識別提供者組配置的用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="c1c93-109">Gets the client secret of the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="c1c93-110">參數</span><span class="sxs-lookup"><span data-stu-id="c1c93-110">PARAMETERS</span></span>

### <span data-ttu-id="c1c93-111">-內容</span><span class="sxs-lookup"><span data-stu-id="c1c93-111">-Context</span></span>
<span data-ttu-id="c1c93-112">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="c1c93-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c1c93-113">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="c1c93-113">This parameter is required.</span></span>

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

### <span data-ttu-id="c1c93-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1c93-114">-DefaultProfile</span></span>
<span data-ttu-id="c1c93-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c1c93-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1c93-116">-類型</span><span class="sxs-lookup"><span data-stu-id="c1c93-116">-Type</span></span>
<span data-ttu-id="c1c93-117">身分識別提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c1c93-117">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="c1c93-118">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="c1c93-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1c93-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1c93-119">CommonParameters</span></span>
<span data-ttu-id="c1c93-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c1c93-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1c93-121">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1c93-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1c93-122">輸入</span><span class="sxs-lookup"><span data-stu-id="c1c93-122">INPUTS</span></span>

### <span data-ttu-id="c1c93-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="c1c93-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c1c93-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="c1c93-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="c1c93-125">輸出</span><span class="sxs-lookup"><span data-stu-id="c1c93-125">OUTPUTS</span></span>

### <span data-ttu-id="c1c93-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementClientSecret</span><span class="sxs-lookup"><span data-stu-id="c1c93-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementClientSecret</span></span>

## <span data-ttu-id="c1c93-127">筆記</span><span class="sxs-lookup"><span data-stu-id="c1c93-127">NOTES</span></span>

## <span data-ttu-id="c1c93-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="c1c93-128">RELATED LINKS</span></span>
