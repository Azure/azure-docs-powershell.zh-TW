---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantAccess.md
ms.openlocfilehash: c0c659f195aa1104b14f41e4cbc82a1ad86a1b1f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970700"
---
# <span data-ttu-id="f4fc3-101">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="f4fc3-101">Get-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="f4fc3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f4fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="f4fc3-103">取得租使用者的存取設定。</span><span class="sxs-lookup"><span data-stu-id="f4fc3-103">Gets the access configuration for a tenant.</span></span>

## <span data-ttu-id="f4fc3-104">句法</span><span class="sxs-lookup"><span data-stu-id="f4fc3-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4fc3-105">說明</span><span class="sxs-lookup"><span data-stu-id="f4fc3-105">DESCRIPTION</span></span>
<span data-ttu-id="f4fc3-106">**AzApiManagementTenantAccess** Cmdlet 會取得租使用者的租使用者存取設定。</span><span class="sxs-lookup"><span data-stu-id="f4fc3-106">The **Get-AzApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>
<span data-ttu-id="f4fc3-107">[結果詳細資料] 中不會包含按鍵。</span><span class="sxs-lookup"><span data-stu-id="f4fc3-107">Keys will not be included into result details.</span></span> <span data-ttu-id="f4fc3-108">若要取得用戶端密碼，請使用 **AzApiManagementTenantAccessSecret** 。</span><span class="sxs-lookup"><span data-stu-id="f4fc3-108">To get client secret, use **Get-AzApiManagementTenantAccessSecret**.</span></span>

## <span data-ttu-id="f4fc3-109">示例</span><span class="sxs-lookup"><span data-stu-id="f4fc3-109">EXAMPLES</span></span>

### <span data-ttu-id="f4fc3-110">範例1：取得租使用者存取設定</span><span class="sxs-lookup"><span data-stu-id="f4fc3-110">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantAccess -Context $apimContext
```

<span data-ttu-id="f4fc3-111">這個命令會取得指定內容的租使用者存取設定。</span><span class="sxs-lookup"><span data-stu-id="f4fc3-111">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="f4fc3-112">參數</span><span class="sxs-lookup"><span data-stu-id="f4fc3-112">PARAMETERS</span></span>

### <span data-ttu-id="f4fc3-113">-內容</span><span class="sxs-lookup"><span data-stu-id="f4fc3-113">-Context</span></span>
<span data-ttu-id="f4fc3-114">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="f4fc3-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f4fc3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4fc3-115">-DefaultProfile</span></span>
<span data-ttu-id="f4fc3-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f4fc3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4fc3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4fc3-117">CommonParameters</span></span>
<span data-ttu-id="f4fc3-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f4fc3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4fc3-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f4fc3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4fc3-120">輸入</span><span class="sxs-lookup"><span data-stu-id="f4fc3-120">INPUTS</span></span>

### <span data-ttu-id="f4fc3-121">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f4fc3-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="f4fc3-122">輸出</span><span class="sxs-lookup"><span data-stu-id="f4fc3-122">OUTPUTS</span></span>

### <span data-ttu-id="f4fc3-123">ServiceManagement. PsApiManagementAccessInformation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f4fc3-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="f4fc3-124">筆記</span><span class="sxs-lookup"><span data-stu-id="f4fc3-124">NOTES</span></span>

## <span data-ttu-id="f4fc3-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="f4fc3-125">RELATED LINKS</span></span>

[<span data-ttu-id="f4fc3-126">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="f4fc3-126">Set-AzApiManagementTenantAccess</span></span>](./Set-AzApiManagementTenantAccess.md)


