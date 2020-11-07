---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
ms.openlocfilehash: 7ca683fc8b4c84a31a651982e5b605d3c29123a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623524"
---
# <span data-ttu-id="0bf28-101">Get-AzureRmApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="0bf28-101">Get-AzureRmApiManagementSsoToken</span></span>

## <span data-ttu-id="0bf28-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0bf28-102">SYNOPSIS</span></span>
<span data-ttu-id="0bf28-103">取得 API 管理服務之已部署管理入口網站的 SSO 標記連結。</span><span class="sxs-lookup"><span data-stu-id="0bf28-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0bf28-104">句法</span><span class="sxs-lookup"><span data-stu-id="0bf28-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bf28-105">說明</span><span class="sxs-lookup"><span data-stu-id="0bf28-105">DESCRIPTION</span></span>
<span data-ttu-id="0bf28-106">**AzureRmApiManagementSsoToken** Cmdlet 會傳回 (URL) 的連結，其中包含單一登入 (SSO) 權杖至 API 管理服務的部署管理入口網站。</span><span class="sxs-lookup"><span data-stu-id="0bf28-106">The **Get-AzureRmApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="0bf28-107">示例</span><span class="sxs-lookup"><span data-stu-id="0bf28-107">EXAMPLES</span></span>

### <span data-ttu-id="0bf28-108">範例1：取得 API 管理服務的 SSO 權杖</span><span class="sxs-lookup"><span data-stu-id="0bf28-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzureRmApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="0bf28-109">這個命令會取得 API 管理服務的 SSO 權杖。</span><span class="sxs-lookup"><span data-stu-id="0bf28-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="0bf28-110">參數</span><span class="sxs-lookup"><span data-stu-id="0bf28-110">PARAMETERS</span></span>

### <span data-ttu-id="0bf28-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="0bf28-111">-Name</span></span>
<span data-ttu-id="0bf28-112">指定 API 管理實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="0bf28-112">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="0bf28-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bf28-113">-ResourceGroupName</span></span>
<span data-ttu-id="0bf28-114">指定 API 管理所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0bf28-114">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="0bf28-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bf28-115">-DefaultProfile</span></span>
<span data-ttu-id="0bf28-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0bf28-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0bf28-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bf28-117">CommonParameters</span></span>
<span data-ttu-id="0bf28-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0bf28-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bf28-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0bf28-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bf28-120">輸入</span><span class="sxs-lookup"><span data-stu-id="0bf28-120">INPUTS</span></span>

## <span data-ttu-id="0bf28-121">輸出</span><span class="sxs-lookup"><span data-stu-id="0bf28-121">OUTPUTS</span></span>

### <span data-ttu-id="0bf28-122">System.object</span><span class="sxs-lookup"><span data-stu-id="0bf28-122">System.String</span></span>

## <span data-ttu-id="0bf28-123">筆記</span><span class="sxs-lookup"><span data-stu-id="0bf28-123">NOTES</span></span>

## <span data-ttu-id="0bf28-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="0bf28-124">RELATED LINKS</span></span>

[<span data-ttu-id="0bf28-125">AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="0bf28-125">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


