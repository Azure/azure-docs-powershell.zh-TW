---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementIdentityProvider.md
ms.openlocfilehash: fe23034b6fc86c9aa76629f806dcb406608f456c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611626"
---
# <span data-ttu-id="480d5-101">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="480d5-101">Get-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="480d5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="480d5-102">SYNOPSIS</span></span>
<span data-ttu-id="480d5-103">取得身分識別提供者設定的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="480d5-103">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="480d5-104">句法</span><span class="sxs-lookup"><span data-stu-id="480d5-104">SYNTAX</span></span>

### <span data-ttu-id="480d5-105">AllIdentityProviders (預設) </span><span class="sxs-lookup"><span data-stu-id="480d5-105">AllIdentityProviders (Default)</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="480d5-106">IdentityProviderByType</span><span class="sxs-lookup"><span data-stu-id="480d5-106">IdentityProviderByType</span></span>
```
Get-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="480d5-107">說明</span><span class="sxs-lookup"><span data-stu-id="480d5-107">DESCRIPTION</span></span>
<span data-ttu-id="480d5-108">取得身分識別提供者設定的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="480d5-108">Get the identity provider configuration details.</span></span>

## <span data-ttu-id="480d5-109">示例</span><span class="sxs-lookup"><span data-stu-id="480d5-109">EXAMPLES</span></span>

### <span data-ttu-id="480d5-110">範例1：取得所有身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="480d5-110">Example 1: Get all Identity Providers</span></span>

```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext
```

<span data-ttu-id="480d5-111">取得服務上的所有身分識別提供者設定。</span><span class="sxs-lookup"><span data-stu-id="480d5-111">Get all the identity provider Configuration on the service.</span></span>

### <span data-ttu-id="480d5-112">取得 AAD 類型身分識別提供者</span><span class="sxs-lookup"><span data-stu-id="480d5-112">Get the AAD Type Identity Provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementIdentityProvider -Context $apimContext -Type Aad
```

<span data-ttu-id="480d5-113">取得 Azure Active Directory 的身分識別提供者設定。</span><span class="sxs-lookup"><span data-stu-id="480d5-113">Gets the Identity Provider Configuration of Azure Active Directory.</span></span>

## <span data-ttu-id="480d5-114">參數</span><span class="sxs-lookup"><span data-stu-id="480d5-114">PARAMETERS</span></span>

### <span data-ttu-id="480d5-115">-內容</span><span class="sxs-lookup"><span data-stu-id="480d5-115">-Context</span></span>
<span data-ttu-id="480d5-116">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="480d5-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="480d5-117">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="480d5-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="480d5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="480d5-118">-DefaultProfile</span></span>
<span data-ttu-id="480d5-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="480d5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="480d5-120">-類型</span><span class="sxs-lookup"><span data-stu-id="480d5-120">-Type</span></span>
<span data-ttu-id="480d5-121">身分識別提供者的識別碼。</span><span class="sxs-lookup"><span data-stu-id="480d5-121">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="480d5-122">如果已指定，將會嘗試透過識別碼尋找身分識別提供者設定。</span><span class="sxs-lookup"><span data-stu-id="480d5-122">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="480d5-123">這個參數是選用的。</span><span class="sxs-lookup"><span data-stu-id="480d5-123">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: IdentityProviderByType
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="480d5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="480d5-124">CommonParameters</span></span>
<span data-ttu-id="480d5-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="480d5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="480d5-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="480d5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="480d5-127">輸入</span><span class="sxs-lookup"><span data-stu-id="480d5-127">INPUTS</span></span>

### <span data-ttu-id="480d5-128">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="480d5-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="480d5-129">ServiceManagement. PsApiManagementIdentityProviderType （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="480d5-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

## <span data-ttu-id="480d5-130">輸出</span><span class="sxs-lookup"><span data-stu-id="480d5-130">OUTPUTS</span></span>

### <span data-ttu-id="480d5-131">ServiceManagement. PsApiManagementIdentityProvider （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="480d5-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="480d5-132">筆記</span><span class="sxs-lookup"><span data-stu-id="480d5-132">NOTES</span></span>

## <span data-ttu-id="480d5-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="480d5-133">RELATED LINKS</span></span>
