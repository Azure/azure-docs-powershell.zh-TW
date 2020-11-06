---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 288EF15B-FE5C-44AE-ABD5-2B92F408B9EB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantsyncstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantSyncState.md
ms.openlocfilehash: 64e1d8ad070d4ce1c2f8129a73efd8730f26d1a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448796"
---
# <span data-ttu-id="b24bc-101">Get-AzureRmApiManagementTenantSyncState</span><span class="sxs-lookup"><span data-stu-id="b24bc-101">Get-AzureRmApiManagementTenantSyncState</span></span>

## <span data-ttu-id="b24bc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b24bc-102">SYNOPSIS</span></span>
<span data-ttu-id="b24bc-103">取得設定資料庫與 Git 儲存庫之間最近同步處理的狀態。</span><span class="sxs-lookup"><span data-stu-id="b24bc-103">Gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b24bc-104">句法</span><span class="sxs-lookup"><span data-stu-id="b24bc-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantSyncState -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b24bc-105">說明</span><span class="sxs-lookup"><span data-stu-id="b24bc-105">DESCRIPTION</span></span>
<span data-ttu-id="b24bc-106">**AzureRmApiManagementTenantSyncState** Cmdlet 會取得設定資料庫與 Git 儲存庫之間最近同步處理的狀態。</span><span class="sxs-lookup"><span data-stu-id="b24bc-106">The **Get-AzureRmApiManagementTenantSyncState** cmdlet gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="b24bc-107">示例</span><span class="sxs-lookup"><span data-stu-id="b24bc-107">EXAMPLES</span></span>

### <span data-ttu-id="b24bc-108">範例1：取得最近同步處理的狀態</span><span class="sxs-lookup"><span data-stu-id="b24bc-108">Example 1: Get the status of the most recent synchronization</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantSyncState -Context $apimContext 
```

<span data-ttu-id="b24bc-109">這個命令會取得設定資料庫與 Git 儲存庫之間最近同步處理的狀態。</span><span class="sxs-lookup"><span data-stu-id="b24bc-109">This command gets the status of the most recent synchronization between the configuration database and the Git repository.</span></span>

## <span data-ttu-id="b24bc-110">參數</span><span class="sxs-lookup"><span data-stu-id="b24bc-110">PARAMETERS</span></span>

### <span data-ttu-id="b24bc-111">-內容</span><span class="sxs-lookup"><span data-stu-id="b24bc-111">-Context</span></span>
<span data-ttu-id="b24bc-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="b24bc-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b24bc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b24bc-113">-DefaultProfile</span></span>
<span data-ttu-id="b24bc-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b24bc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="b24bc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b24bc-115">CommonParameters</span></span>
<span data-ttu-id="b24bc-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b24bc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b24bc-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b24bc-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b24bc-118">輸入</span><span class="sxs-lookup"><span data-stu-id="b24bc-118">INPUTS</span></span>

### <span data-ttu-id="b24bc-119">所有</span><span class="sxs-lookup"><span data-stu-id="b24bc-119">None</span></span>
<span data-ttu-id="b24bc-120">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="b24bc-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b24bc-121">輸出</span><span class="sxs-lookup"><span data-stu-id="b24bc-121">OUTPUTS</span></span>

### <span data-ttu-id="b24bc-122">ServiceManagement. PsApiManagementAccessInformation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="b24bc-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="b24bc-123">筆記</span><span class="sxs-lookup"><span data-stu-id="b24bc-123">NOTES</span></span>

## <span data-ttu-id="b24bc-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="b24bc-124">RELATED LINKS</span></span>

