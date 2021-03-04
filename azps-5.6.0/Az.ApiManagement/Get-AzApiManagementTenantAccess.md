---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: c19888bd45ae943b60b90172913a83f42a1fd6f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915686"
---
# <span data-ttu-id="4794f-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="4794f-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="4794f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4794f-102">SYNOPSIS</span></span>
<span data-ttu-id="4794f-103">取得租使用者的存取權限組。</span><span class="sxs-lookup"><span data-stu-id="4794f-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="4794f-104">語法</span><span class="sxs-lookup"><span data-stu-id="4794f-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4794f-105">描述</span><span class="sxs-lookup"><span data-stu-id="4794f-105">DESCRIPTION</span></span>
<span data-ttu-id="4794f-106">**Get-AzApiManagementTenantAccess** Cmdlet 會取得租使用者之租使用者存取設置。</span><span class="sxs-lookup"><span data-stu-id="4794f-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>
<span data-ttu-id="4794f-107">按鍵不會包含在結果詳細資料中。</span><span class="sxs-lookup"><span data-stu-id="4794f-107">Keys will not be included into result details.</span></span> <span data-ttu-id="4794f-108">若要取得用戶端機密，請使用 **Get-AzApiManagementTenantAccessSecret。**</span><span class="sxs-lookup"><span data-stu-id="4794f-108">To get client secret, use **Get-AzApiManagementTenantAccessSecret**.</span></span>

## <span data-ttu-id="4794f-109">例子</span><span class="sxs-lookup"><span data-stu-id="4794f-109">EXAMPLES</span></span>

### <span data-ttu-id="4794f-110">範例 1：取得租使用者存取組</span><span class="sxs-lookup"><span data-stu-id="4794f-110">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="4794f-111">此命令會取得指定上下文的租使用者存取組。</span><span class="sxs-lookup"><span data-stu-id="4794f-111">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="4794f-112">參數</span><span class="sxs-lookup"><span data-stu-id="4794f-112">PARAMETERS</span></span>

### <span data-ttu-id="4794f-113">-內容</span><span class="sxs-lookup"><span data-stu-id="4794f-113">-Context</span></span>
<span data-ttu-id="4794f-114">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="4794f-114">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4794f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4794f-115">-DefaultProfile</span></span>
<span data-ttu-id="4794f-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4794f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4794f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4794f-117">CommonParameters</span></span>
<span data-ttu-id="4794f-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4794f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4794f-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4794f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4794f-120">輸入</span><span class="sxs-lookup"><span data-stu-id="4794f-120">INPUTS</span></span>

### <span data-ttu-id="4794f-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="4794f-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="4794f-122">輸出</span><span class="sxs-lookup"><span data-stu-id="4794f-122">OUTPUTS</span></span>

### <span data-ttu-id="4794f-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="4794f-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="4794f-124">筆記</span><span class="sxs-lookup"><span data-stu-id="4794f-124">NOTES</span></span>

## <span data-ttu-id="4794f-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="4794f-125">RELATED LINKS</span></span>

[<span data-ttu-id="4794f-126">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="4794f-126">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


