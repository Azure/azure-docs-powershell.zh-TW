---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: 010e52d7c2d05977c8125d5d78d69ef8ac7f75fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623442"
---
# <span data-ttu-id="eaaa1-101">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="eaaa1-101">Get-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="eaaa1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eaaa1-102">SYNOPSIS</span></span>
<span data-ttu-id="eaaa1-103">取得租使用者的存取設定。</span><span class="sxs-lookup"><span data-stu-id="eaaa1-103">Gets the access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaaa1-104">句法</span><span class="sxs-lookup"><span data-stu-id="eaaa1-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eaaa1-105">說明</span><span class="sxs-lookup"><span data-stu-id="eaaa1-105">DESCRIPTION</span></span>
<span data-ttu-id="eaaa1-106">**AzureRmApiManagementTenantAccess** Cmdlet 會取得租使用者的租使用者存取設定。</span><span class="sxs-lookup"><span data-stu-id="eaaa1-106">The **Get-AzureRmApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="eaaa1-107">示例</span><span class="sxs-lookup"><span data-stu-id="eaaa1-107">EXAMPLES</span></span>

### <span data-ttu-id="eaaa1-108">範例1：取得租使用者存取設定</span><span class="sxs-lookup"><span data-stu-id="eaaa1-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="eaaa1-109">這個命令會取得指定內容的租使用者存取設定。</span><span class="sxs-lookup"><span data-stu-id="eaaa1-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="eaaa1-110">參數</span><span class="sxs-lookup"><span data-stu-id="eaaa1-110">PARAMETERS</span></span>

### <span data-ttu-id="eaaa1-111">-內容</span><span class="sxs-lookup"><span data-stu-id="eaaa1-111">-Context</span></span>
<span data-ttu-id="eaaa1-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="eaaa1-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="eaaa1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaaa1-113">-DefaultProfile</span></span>
<span data-ttu-id="eaaa1-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="eaaa1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaaa1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaaa1-115">CommonParameters</span></span>
<span data-ttu-id="eaaa1-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eaaa1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaaa1-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eaaa1-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaaa1-118">輸入</span><span class="sxs-lookup"><span data-stu-id="eaaa1-118">INPUTS</span></span>

### <span data-ttu-id="eaaa1-119">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="eaaa1-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="eaaa1-120">輸出</span><span class="sxs-lookup"><span data-stu-id="eaaa1-120">OUTPUTS</span></span>

### <span data-ttu-id="eaaa1-121">ServiceManagement. PsApiManagementAccessInformation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="eaaa1-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="eaaa1-122">筆記</span><span class="sxs-lookup"><span data-stu-id="eaaa1-122">NOTES</span></span>

## <span data-ttu-id="eaaa1-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="eaaa1-123">RELATED LINKS</span></span>

[<span data-ttu-id="eaaa1-124">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="eaaa1-124">Set-AzureRmApiManagementTenantAccess</span></span>](./Set-AzureRmApiManagementTenantAccess.md)


