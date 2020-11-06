---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantGitAccess.md
ms.openlocfilehash: 643877de4ab2b9107459beaa7acb276072a249ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448498"
---
# <span data-ttu-id="b247b-101">Get-AzureRmApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="b247b-101">Get-AzureRmApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="b247b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b247b-102">SYNOPSIS</span></span>
<span data-ttu-id="b247b-103">取得租使用者的 Git 存取設定。</span><span class="sxs-lookup"><span data-stu-id="b247b-103">Gets the Git access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b247b-104">句法</span><span class="sxs-lookup"><span data-stu-id="b247b-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantGitAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b247b-105">說明</span><span class="sxs-lookup"><span data-stu-id="b247b-105">DESCRIPTION</span></span>
<span data-ttu-id="b247b-106">**AzureRmApiManagementTenantGitAccess** Cmdlet 會取得租使用者的 Git 存取設定。</span><span class="sxs-lookup"><span data-stu-id="b247b-106">The **Get-AzureRmApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="b247b-107">示例</span><span class="sxs-lookup"><span data-stu-id="b247b-107">EXAMPLES</span></span>

### <span data-ttu-id="b247b-108">範例1：取得租使用者存取設定</span><span class="sxs-lookup"><span data-stu-id="b247b-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantGitAccess -Context $apimContext
```

<span data-ttu-id="b247b-109">這個命令會取得指定內容的 Git 存取設定。</span><span class="sxs-lookup"><span data-stu-id="b247b-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="b247b-110">參數</span><span class="sxs-lookup"><span data-stu-id="b247b-110">PARAMETERS</span></span>

### <span data-ttu-id="b247b-111">-內容</span><span class="sxs-lookup"><span data-stu-id="b247b-111">-Context</span></span>
<span data-ttu-id="b247b-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="b247b-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b247b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b247b-113">-DefaultProfile</span></span>
<span data-ttu-id="b247b-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b247b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b247b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b247b-115">CommonParameters</span></span>
<span data-ttu-id="b247b-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b247b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b247b-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b247b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b247b-118">輸入</span><span class="sxs-lookup"><span data-stu-id="b247b-118">INPUTS</span></span>

### <span data-ttu-id="b247b-119">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="b247b-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="b247b-120">輸出</span><span class="sxs-lookup"><span data-stu-id="b247b-120">OUTPUTS</span></span>

### <span data-ttu-id="b247b-121">ServiceManagement. PsApiManagementAccessInformation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="b247b-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="b247b-122">筆記</span><span class="sxs-lookup"><span data-stu-id="b247b-122">NOTES</span></span>

## <span data-ttu-id="b247b-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="b247b-123">RELATED LINKS</span></span>
