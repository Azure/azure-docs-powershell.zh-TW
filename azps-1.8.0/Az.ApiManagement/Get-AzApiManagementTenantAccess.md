---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: 2418ec3f5e9570046c37c76bdaef8f853ff819b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611607"
---
# <span data-ttu-id="e5ecf-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="e5ecf-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="e5ecf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="e5ecf-103">取得租使用者的存取設定。</span><span class="sxs-lookup"><span data-stu-id="e5ecf-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="e5ecf-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5ecf-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5ecf-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5ecf-105">DESCRIPTION</span></span>
<span data-ttu-id="e5ecf-106">**AzApiManagementTenantAccess** Cmdlet 會取得租使用者的租使用者存取設定。</span><span class="sxs-lookup"><span data-stu-id="e5ecf-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="e5ecf-107">示例</span><span class="sxs-lookup"><span data-stu-id="e5ecf-107">EXAMPLES</span></span>

### <span data-ttu-id="e5ecf-108">範例1：取得租使用者存取設定</span><span class="sxs-lookup"><span data-stu-id="e5ecf-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="e5ecf-109">這個命令會取得指定內容的租使用者存取設定。</span><span class="sxs-lookup"><span data-stu-id="e5ecf-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="e5ecf-110">參數</span><span class="sxs-lookup"><span data-stu-id="e5ecf-110">PARAMETERS</span></span>

### <span data-ttu-id="e5ecf-111">-內容</span><span class="sxs-lookup"><span data-stu-id="e5ecf-111">-Context</span></span>
<span data-ttu-id="e5ecf-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="e5ecf-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e5ecf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5ecf-113">-DefaultProfile</span></span>
<span data-ttu-id="e5ecf-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e5ecf-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5ecf-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5ecf-115">CommonParameters</span></span>
<span data-ttu-id="e5ecf-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5ecf-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5ecf-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5ecf-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5ecf-118">輸入</span><span class="sxs-lookup"><span data-stu-id="e5ecf-118">INPUTS</span></span>

### <span data-ttu-id="e5ecf-119">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e5ecf-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="e5ecf-120">輸出</span><span class="sxs-lookup"><span data-stu-id="e5ecf-120">OUTPUTS</span></span>

### <span data-ttu-id="e5ecf-121">ServiceManagement. PsApiManagementAccessInformation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e5ecf-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="e5ecf-122">筆記</span><span class="sxs-lookup"><span data-stu-id="e5ecf-122">NOTES</span></span>

## <span data-ttu-id="e5ecf-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5ecf-123">RELATED LINKS</span></span>

[<span data-ttu-id="e5ecf-124">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="e5ecf-124">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


