---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSsoToken.md
ms.openlocfilehash: 927343f6a80edb82b933bfa382bbf6b690b90f07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448801"
---
# <span data-ttu-id="3369e-101">Get-AzureRmApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="3369e-101">Get-AzureRmApiManagementSsoToken</span></span>

## <span data-ttu-id="3369e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3369e-102">SYNOPSIS</span></span>
<span data-ttu-id="3369e-103">取得 API 管理服務之已部署管理入口網站的 SSO 標記連結。</span><span class="sxs-lookup"><span data-stu-id="3369e-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3369e-104">句法</span><span class="sxs-lookup"><span data-stu-id="3369e-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3369e-105">說明</span><span class="sxs-lookup"><span data-stu-id="3369e-105">DESCRIPTION</span></span>
<span data-ttu-id="3369e-106">**AzureRmApiManagementSsoToken** Cmdlet 會傳回 (URL) 的連結，其中包含單一登入 (SSO) 權杖至 API 管理服務的部署管理入口網站。</span><span class="sxs-lookup"><span data-stu-id="3369e-106">The **Get-AzureRmApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="3369e-107">示例</span><span class="sxs-lookup"><span data-stu-id="3369e-107">EXAMPLES</span></span>

### <span data-ttu-id="3369e-108">範例1：取得 API 管理服務的 SSO 權杖</span><span class="sxs-lookup"><span data-stu-id="3369e-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzureRmApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="3369e-109">這個命令會取得 API 管理服務的 SSO 權杖。</span><span class="sxs-lookup"><span data-stu-id="3369e-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="3369e-110">參數</span><span class="sxs-lookup"><span data-stu-id="3369e-110">PARAMETERS</span></span>

### <span data-ttu-id="3369e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3369e-111">-DefaultProfile</span></span>
<span data-ttu-id="3369e-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3369e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3369e-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="3369e-113">-Name</span></span>
<span data-ttu-id="3369e-114">指定 API 管理實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="3369e-114">Specifies the name of the API Management instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3369e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3369e-115">-ResourceGroupName</span></span>
<span data-ttu-id="3369e-116">指定 API 管理所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3369e-116">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3369e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3369e-117">CommonParameters</span></span>
<span data-ttu-id="3369e-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3369e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3369e-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3369e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3369e-120">輸入</span><span class="sxs-lookup"><span data-stu-id="3369e-120">INPUTS</span></span>

### <span data-ttu-id="3369e-121">所有</span><span class="sxs-lookup"><span data-stu-id="3369e-121">None</span></span>
<span data-ttu-id="3369e-122">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="3369e-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3369e-123">輸出</span><span class="sxs-lookup"><span data-stu-id="3369e-123">OUTPUTS</span></span>

### <span data-ttu-id="3369e-124">System.object</span><span class="sxs-lookup"><span data-stu-id="3369e-124">System.String</span></span>

## <span data-ttu-id="3369e-125">筆記</span><span class="sxs-lookup"><span data-stu-id="3369e-125">NOTES</span></span>

## <span data-ttu-id="3369e-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="3369e-126">RELATED LINKS</span></span>

[<span data-ttu-id="3369e-127">AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="3369e-127">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


