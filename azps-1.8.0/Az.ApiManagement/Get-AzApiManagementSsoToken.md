---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 40c9166ab650f7cb31ac53c55397bb7bc635f6e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611608"
---
# <span data-ttu-id="52fd7-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="52fd7-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="52fd7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52fd7-102">SYNOPSIS</span></span>
<span data-ttu-id="52fd7-103">取得 API 管理服務之已部署管理入口網站的 SSO 標記連結。</span><span class="sxs-lookup"><span data-stu-id="52fd7-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="52fd7-104">句法</span><span class="sxs-lookup"><span data-stu-id="52fd7-104">SYNTAX</span></span>

```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52fd7-105">說明</span><span class="sxs-lookup"><span data-stu-id="52fd7-105">DESCRIPTION</span></span>
<span data-ttu-id="52fd7-106">**AzApiManagementSsoToken** Cmdlet 會傳回 (URL) 的連結，其中包含單一登入 (SSO) 權杖至 API 管理服務的部署管理入口網站。</span><span class="sxs-lookup"><span data-stu-id="52fd7-106">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="52fd7-107">示例</span><span class="sxs-lookup"><span data-stu-id="52fd7-107">EXAMPLES</span></span>

### <span data-ttu-id="52fd7-108">範例1：取得 API 管理服務的 SSO 權杖</span><span class="sxs-lookup"><span data-stu-id="52fd7-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="52fd7-109">這個命令會取得 API 管理服務的 SSO 權杖。</span><span class="sxs-lookup"><span data-stu-id="52fd7-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="52fd7-110">參數</span><span class="sxs-lookup"><span data-stu-id="52fd7-110">PARAMETERS</span></span>

### <span data-ttu-id="52fd7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52fd7-111">-DefaultProfile</span></span>
<span data-ttu-id="52fd7-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="52fd7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52fd7-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="52fd7-113">-Name</span></span>
<span data-ttu-id="52fd7-114">指定 API 管理實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="52fd7-114">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="52fd7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52fd7-115">-ResourceGroupName</span></span>
<span data-ttu-id="52fd7-116">指定 API 管理所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="52fd7-116">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="52fd7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52fd7-117">CommonParameters</span></span>
<span data-ttu-id="52fd7-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52fd7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52fd7-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="52fd7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52fd7-120">輸入</span><span class="sxs-lookup"><span data-stu-id="52fd7-120">INPUTS</span></span>

### <span data-ttu-id="52fd7-121">System.object</span><span class="sxs-lookup"><span data-stu-id="52fd7-121">System.String</span></span>

## <span data-ttu-id="52fd7-122">輸出</span><span class="sxs-lookup"><span data-stu-id="52fd7-122">OUTPUTS</span></span>

### <span data-ttu-id="52fd7-123">System.object</span><span class="sxs-lookup"><span data-stu-id="52fd7-123">System.String</span></span>

## <span data-ttu-id="52fd7-124">筆記</span><span class="sxs-lookup"><span data-stu-id="52fd7-124">NOTES</span></span>

## <span data-ttu-id="52fd7-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="52fd7-125">RELATED LINKS</span></span>

[<span data-ttu-id="52fd7-126">AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="52fd7-126">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)


