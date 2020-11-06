---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
ms.openlocfilehash: 56dc320ea6aafd37e93912071a3256040342e2db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452907"
---
# <span data-ttu-id="17d86-101">New-AzureRmApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="17d86-101">New-AzureRmApiManagementContext</span></span>

## <span data-ttu-id="17d86-102">摘要</span><span class="sxs-lookup"><span data-stu-id="17d86-102">SYNOPSIS</span></span>
<span data-ttu-id="17d86-103">建立 PsAzureApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="17d86-103">Creates an instance of PsAzureApiManagementContext.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17d86-104">句法</span><span class="sxs-lookup"><span data-stu-id="17d86-104">SYNTAX</span></span>

```
New-AzureRmApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17d86-105">說明</span><span class="sxs-lookup"><span data-stu-id="17d86-105">DESCRIPTION</span></span>
<span data-ttu-id="17d86-106">**新的-AzureRmApiManagementCoNtext** Cmdlet 會建立 **PsAzureApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="17d86-106">The **New-AzureRmApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="17d86-107">此內容用於所有 API 管理服務 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="17d86-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="17d86-108">示例</span><span class="sxs-lookup"><span data-stu-id="17d86-108">EXAMPLES</span></span>

### <span data-ttu-id="17d86-109">範例1：建立 PsApiManagementCoNtext 實例</span><span class="sxs-lookup"><span data-stu-id="17d86-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="17d86-110">這個命令會建立 **PsApiManagementCoNtext** 的實例。</span><span class="sxs-lookup"><span data-stu-id="17d86-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="17d86-111">參數</span><span class="sxs-lookup"><span data-stu-id="17d86-111">PARAMETERS</span></span>

### <span data-ttu-id="17d86-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17d86-112">-DefaultProfile</span></span>
<span data-ttu-id="17d86-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="17d86-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17d86-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17d86-114">-ResourceGroupName</span></span>
<span data-ttu-id="17d86-115">指定部署 API 管理服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="17d86-115">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="17d86-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="17d86-116">-ServiceName</span></span>
<span data-ttu-id="17d86-117">指定已部署 API 管理服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="17d86-117">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="17d86-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17d86-118">CommonParameters</span></span>
<span data-ttu-id="17d86-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="17d86-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17d86-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="17d86-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17d86-121">輸入</span><span class="sxs-lookup"><span data-stu-id="17d86-121">INPUTS</span></span>

### <span data-ttu-id="17d86-122">System.object</span><span class="sxs-lookup"><span data-stu-id="17d86-122">System.String</span></span>

## <span data-ttu-id="17d86-123">輸出</span><span class="sxs-lookup"><span data-stu-id="17d86-123">OUTPUTS</span></span>

### <span data-ttu-id="17d86-124">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="17d86-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="17d86-125">筆記</span><span class="sxs-lookup"><span data-stu-id="17d86-125">NOTES</span></span>

## <span data-ttu-id="17d86-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="17d86-126">RELATED LINKS</span></span>
