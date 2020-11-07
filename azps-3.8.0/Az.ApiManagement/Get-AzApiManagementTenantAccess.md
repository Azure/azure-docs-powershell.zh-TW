---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: 3c4151cbc6b170f8b34e70126f37e4478933744d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956874"
---
# <span data-ttu-id="7d830-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="7d830-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="7d830-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d830-102">SYNOPSIS</span></span>
<span data-ttu-id="7d830-103">取得租使用者的存取設定。</span><span class="sxs-lookup"><span data-stu-id="7d830-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="7d830-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d830-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d830-105">說明</span><span class="sxs-lookup"><span data-stu-id="7d830-105">DESCRIPTION</span></span>
<span data-ttu-id="7d830-106">**AzApiManagementTenantAccess** Cmdlet 會取得租使用者的租使用者存取設定。</span><span class="sxs-lookup"><span data-stu-id="7d830-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="7d830-107">示例</span><span class="sxs-lookup"><span data-stu-id="7d830-107">EXAMPLES</span></span>

### <span data-ttu-id="7d830-108">範例1：取得租使用者存取設定</span><span class="sxs-lookup"><span data-stu-id="7d830-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="7d830-109">這個命令會取得指定內容的租使用者存取設定。</span><span class="sxs-lookup"><span data-stu-id="7d830-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="7d830-110">參數</span><span class="sxs-lookup"><span data-stu-id="7d830-110">PARAMETERS</span></span>

### <span data-ttu-id="7d830-111">-內容</span><span class="sxs-lookup"><span data-stu-id="7d830-111">-Context</span></span>
<span data-ttu-id="7d830-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="7d830-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7d830-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d830-113">-DefaultProfile</span></span>
<span data-ttu-id="7d830-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7d830-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d830-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d830-115">CommonParameters</span></span>
<span data-ttu-id="7d830-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d830-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d830-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7d830-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d830-118">輸入</span><span class="sxs-lookup"><span data-stu-id="7d830-118">INPUTS</span></span>

### <span data-ttu-id="7d830-119">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="7d830-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="7d830-120">輸出</span><span class="sxs-lookup"><span data-stu-id="7d830-120">OUTPUTS</span></span>

### <span data-ttu-id="7d830-121">ServiceManagement. PsApiManagementAccessInformation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="7d830-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="7d830-122">筆記</span><span class="sxs-lookup"><span data-stu-id="7d830-122">NOTES</span></span>

## <span data-ttu-id="7d830-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d830-123">RELATED LINKS</span></span>

[<span data-ttu-id="7d830-124">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="7d830-124">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


