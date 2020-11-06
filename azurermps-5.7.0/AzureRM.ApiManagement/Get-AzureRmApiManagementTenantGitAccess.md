---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
ms.openlocfilehash: 28b27ee7a2e24b425d5ffa93be4d1f3513a31c08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448799"
---
# <span data-ttu-id="f9b02-101">Get-AzureRmApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="f9b02-101">Get-AzureRmApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="f9b02-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9b02-102">SYNOPSIS</span></span>
<span data-ttu-id="f9b02-103">取得租使用者的 Git 存取設定。</span><span class="sxs-lookup"><span data-stu-id="f9b02-103">Gets the Git access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9b02-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9b02-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantGitAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9b02-105">說明</span><span class="sxs-lookup"><span data-stu-id="f9b02-105">DESCRIPTION</span></span>
<span data-ttu-id="f9b02-106">**AzureRmApiManagementTenantGitAccess** Cmdlet 會取得租使用者的 Git 存取設定。</span><span class="sxs-lookup"><span data-stu-id="f9b02-106">The **Get-AzureRmApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="f9b02-107">示例</span><span class="sxs-lookup"><span data-stu-id="f9b02-107">EXAMPLES</span></span>

### <span data-ttu-id="f9b02-108">範例1：取得租使用者存取設定</span><span class="sxs-lookup"><span data-stu-id="f9b02-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantGitAccess -Context $apimContext 
```

<span data-ttu-id="f9b02-109">這個命令會取得指定內容的 Git 存取設定。</span><span class="sxs-lookup"><span data-stu-id="f9b02-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="f9b02-110">參數</span><span class="sxs-lookup"><span data-stu-id="f9b02-110">PARAMETERS</span></span>

### <span data-ttu-id="f9b02-111">-內容</span><span class="sxs-lookup"><span data-stu-id="f9b02-111">-Context</span></span>
<span data-ttu-id="f9b02-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="f9b02-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f9b02-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9b02-113">-DefaultProfile</span></span>
<span data-ttu-id="f9b02-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9b02-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="f9b02-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9b02-115">CommonParameters</span></span>
<span data-ttu-id="f9b02-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9b02-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9b02-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f9b02-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9b02-118">輸入</span><span class="sxs-lookup"><span data-stu-id="f9b02-118">INPUTS</span></span>

### <span data-ttu-id="f9b02-119">所有</span><span class="sxs-lookup"><span data-stu-id="f9b02-119">None</span></span>
<span data-ttu-id="f9b02-120">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="f9b02-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f9b02-121">輸出</span><span class="sxs-lookup"><span data-stu-id="f9b02-121">OUTPUTS</span></span>

### <span data-ttu-id="f9b02-122">ServiceManagement. PsApiManagementAccessInformation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f9b02-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="f9b02-123">筆記</span><span class="sxs-lookup"><span data-stu-id="f9b02-123">NOTES</span></span>

## <span data-ttu-id="f9b02-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9b02-124">RELATED LINKS</span></span>

