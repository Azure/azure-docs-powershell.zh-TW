---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8B0116E5-0AED-4050-BF11-1BFE65DB9436
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 3c37376aa475e8b0797d4ff4433ab54a11d2b6bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450943"
---
# <span data-ttu-id="bf68f-101">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="bf68f-101">Get-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="bf68f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf68f-102">SYNOPSIS</span></span>
<span data-ttu-id="bf68f-103">取得 API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="bf68f-103">Gets an API Management authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf68f-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf68f-104">SYNTAX</span></span>

### <span data-ttu-id="bf68f-105">取得所有授權伺服器 (預設) </span><span class="sxs-lookup"><span data-stu-id="bf68f-105">Get all authorization server (Default)</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf68f-106">依識別碼取得</span><span class="sxs-lookup"><span data-stu-id="bf68f-106">Get by Id</span></span>
```
Get-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> [-ServerId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf68f-107">說明</span><span class="sxs-lookup"><span data-stu-id="bf68f-107">DESCRIPTION</span></span>
<span data-ttu-id="bf68f-108">**AzureRmApiManagementAuthorizationServer** Cmdlet 會取得所有 Azure API 管理授權伺服器或指定的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="bf68f-108">The **Get-AzureRmApiManagementAuthorizationServer** cmdlet gets all Azure API Management authorization servers or specified authorization servers.</span></span>

## <span data-ttu-id="bf68f-109">示例</span><span class="sxs-lookup"><span data-stu-id="bf68f-109">EXAMPLES</span></span>

### <span data-ttu-id="bf68f-110">範例1：取得所有授權伺服器</span><span class="sxs-lookup"><span data-stu-id="bf68f-110">Example 1: Get all authorization servers</span></span>
```
PS C:\>Get-AzureRmApiManagementAuthrizarionServer -Context $ApiMgmtContext
```

<span data-ttu-id="bf68f-111">這個命令會取得所有 API 管理授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="bf68f-111">This command gets all API Management authorization servers.</span></span>

### <span data-ttu-id="bf68f-112">範例2：取得指定的授權伺服器</span><span class="sxs-lookup"><span data-stu-id="bf68f-112">Example 2: Get a specified authorization server</span></span>
```
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -ServerId "0123456789"
```

<span data-ttu-id="bf68f-113">這個命令會取得指定的授權伺服器。</span><span class="sxs-lookup"><span data-stu-id="bf68f-113">This command gets the specified authorization server.</span></span>

## <span data-ttu-id="bf68f-114">參數</span><span class="sxs-lookup"><span data-stu-id="bf68f-114">PARAMETERS</span></span>

### <span data-ttu-id="bf68f-115">-內容</span><span class="sxs-lookup"><span data-stu-id="bf68f-115">-Context</span></span>
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

### <span data-ttu-id="bf68f-116">-ServerId</span><span class="sxs-lookup"><span data-stu-id="bf68f-116">-ServerId</span></span>
```yaml
Type: System.String
Parameter Sets: Get by Id
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf68f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf68f-117">-DefaultProfile</span></span>
<span data-ttu-id="bf68f-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bf68f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf68f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf68f-119">CommonParameters</span></span>
<span data-ttu-id="bf68f-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf68f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf68f-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bf68f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf68f-122">輸入</span><span class="sxs-lookup"><span data-stu-id="bf68f-122">INPUTS</span></span>

## <span data-ttu-id="bf68f-123">輸出</span><span class="sxs-lookup"><span data-stu-id="bf68f-123">OUTPUTS</span></span>

### <span data-ttu-id="bf68f-124">IList<ApiManagement. ServiceManagement. PsApiManagementOAuth2AuthrozationServer]></span><span class="sxs-lookup"><span data-stu-id="bf68f-124">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOAuth2AuthrozationServer></span></span>

## <span data-ttu-id="bf68f-125">筆記</span><span class="sxs-lookup"><span data-stu-id="bf68f-125">NOTES</span></span>

## <span data-ttu-id="bf68f-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf68f-126">RELATED LINKS</span></span>

[<span data-ttu-id="bf68f-127">新-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="bf68f-127">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="bf68f-128">移除-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="bf68f-128">Remove-AzureRmApiManagementAuthorizationServer</span></span>](./Remove-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="bf68f-129">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="bf68f-129">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


