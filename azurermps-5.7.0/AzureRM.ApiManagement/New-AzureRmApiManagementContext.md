---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
ms.openlocfilehash: da9924624065937a0cb2d78160b1a12cb698a42d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448790"
---
# <span data-ttu-id="2a718-101">New-AzureRmApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2a718-101">New-AzureRmApiManagementContext</span></span>

## <span data-ttu-id="2a718-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2a718-102">SYNOPSIS</span></span>
<span data-ttu-id="2a718-103">建立 PsAzureApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="2a718-103">Creates an instance of PsAzureApiManagementContext.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a718-104">句法</span><span class="sxs-lookup"><span data-stu-id="2a718-104">SYNTAX</span></span>

```
New-AzureRmApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a718-105">說明</span><span class="sxs-lookup"><span data-stu-id="2a718-105">DESCRIPTION</span></span>
<span data-ttu-id="2a718-106">**新的-AzureRmApiManagementCoNtext** Cmdlet 會建立 **PsAzureApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="2a718-106">The **New-AzureRmApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="2a718-107">此內容用於所有 API 管理服務 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a718-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="2a718-108">示例</span><span class="sxs-lookup"><span data-stu-id="2a718-108">EXAMPLES</span></span>

### <span data-ttu-id="2a718-109">範例1：建立 PsApiManagementCoNtext 實例</span><span class="sxs-lookup"><span data-stu-id="2a718-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="2a718-110">這個命令會建立 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="2a718-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="2a718-111">參數</span><span class="sxs-lookup"><span data-stu-id="2a718-111">PARAMETERS</span></span>

### <span data-ttu-id="2a718-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a718-112">-DefaultProfile</span></span>
<span data-ttu-id="2a718-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a718-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="2a718-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a718-114">-ResourceGroupName</span></span>
<span data-ttu-id="2a718-115">指定部署 API 管理服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a718-115">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="2a718-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2a718-116">-ServiceName</span></span>
<span data-ttu-id="2a718-117">指定已部署 API 管理服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a718-117">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="2a718-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a718-118">CommonParameters</span></span>
<span data-ttu-id="2a718-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2a718-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a718-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2a718-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a718-121">輸入</span><span class="sxs-lookup"><span data-stu-id="2a718-121">INPUTS</span></span>

### <span data-ttu-id="2a718-122">所有</span><span class="sxs-lookup"><span data-stu-id="2a718-122">None</span></span>
<span data-ttu-id="2a718-123">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2a718-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2a718-124">輸出</span><span class="sxs-lookup"><span data-stu-id="2a718-124">OUTPUTS</span></span>

### <span data-ttu-id="2a718-125">ServiceManagement. PsAzureApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="2a718-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsAzureApiManagementContext</span></span>

## <span data-ttu-id="2a718-126">筆記</span><span class="sxs-lookup"><span data-stu-id="2a718-126">NOTES</span></span>

## <span data-ttu-id="2a718-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a718-127">RELATED LINKS</span></span>

