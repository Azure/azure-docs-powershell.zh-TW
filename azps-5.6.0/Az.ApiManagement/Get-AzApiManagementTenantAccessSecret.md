---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccessSecret.md
ms.openlocfilehash: 56246de86606aeb07dd8ccdbcfbf2dc35b32a5a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915678"
---
# <span data-ttu-id="b6bbf-101">Get-AzApiManagementTenantAccessSecret</span><span class="sxs-lookup"><span data-stu-id="b6bbf-101">Get-AzApiManagementTenantAccessSecret</span></span>

## <span data-ttu-id="b6bbf-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b6bbf-102">SYNOPSIS</span></span>
<span data-ttu-id="b6bbf-103">取得租使用者的存取權限組組鍵。</span><span class="sxs-lookup"><span data-stu-id="b6bbf-103">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="b6bbf-104">語法</span><span class="sxs-lookup"><span data-stu-id="b6bbf-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6bbf-105">描述</span><span class="sxs-lookup"><span data-stu-id="b6bbf-105">DESCRIPTION</span></span>
<span data-ttu-id="b6bbf-106">取得租使用者的存取權限組組鍵。</span><span class="sxs-lookup"><span data-stu-id="b6bbf-106">Gets the access configuration keys for a tenant.</span></span>

## <span data-ttu-id="b6bbf-107">例子</span><span class="sxs-lookup"><span data-stu-id="b6bbf-107">EXAMPLES</span></span>

### <span data-ttu-id="b6bbf-108">範例 1：取得租使用者存取組組鍵</span><span class="sxs-lookup"><span data-stu-id="b6bbf-108">Example 1: Get tenant access configuration keys</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccessSecret -Context $apimContext
```

<span data-ttu-id="b6bbf-109">此命令會取得指定上下文的租使用者存取組組鍵。</span><span class="sxs-lookup"><span data-stu-id="b6bbf-109">This command gets the tenant access configuration keys for the specified context.</span></span>

## <span data-ttu-id="b6bbf-110">參數</span><span class="sxs-lookup"><span data-stu-id="b6bbf-110">PARAMETERS</span></span>

### <span data-ttu-id="b6bbf-111">-內容</span><span class="sxs-lookup"><span data-stu-id="b6bbf-111">-Context</span></span>
<span data-ttu-id="b6bbf-112">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="b6bbf-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b6bbf-113">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="b6bbf-113">This parameter is required.</span></span>

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

### <span data-ttu-id="b6bbf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6bbf-114">-DefaultProfile</span></span>
<span data-ttu-id="b6bbf-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6bbf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6bbf-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6bbf-116">CommonParameters</span></span>
<span data-ttu-id="b6bbf-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b6bbf-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6bbf-118">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6bbf-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6bbf-119">輸入</span><span class="sxs-lookup"><span data-stu-id="b6bbf-119">INPUTS</span></span>

### <span data-ttu-id="b6bbf-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="b6bbf-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="b6bbf-121">輸出</span><span class="sxs-lookup"><span data-stu-id="b6bbf-121">OUTPUTS</span></span>

### <span data-ttu-id="b6bbf-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="b6bbf-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="b6bbf-123">筆記</span><span class="sxs-lookup"><span data-stu-id="b6bbf-123">NOTES</span></span>

## <span data-ttu-id="b6bbf-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6bbf-124">RELATED LINKS</span></span>
