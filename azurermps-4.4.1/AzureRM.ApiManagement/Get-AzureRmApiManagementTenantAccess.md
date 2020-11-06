---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 236B4436-E8AD-42B4-922C-E2E1406CAFC2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: 30243ef1796e621d0898aae38e29ddb1dc7fd20b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93454968"
---
# <span data-ttu-id="11c87-101">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="11c87-101">Get-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="11c87-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11c87-102">SYNOPSIS</span></span>
<span data-ttu-id="11c87-103">取得租使用者的存取設定。</span><span class="sxs-lookup"><span data-stu-id="11c87-103">Gets the access configuration for a tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11c87-104">句法</span><span class="sxs-lookup"><span data-stu-id="11c87-104">SYNTAX</span></span>

```
Get-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11c87-105">說明</span><span class="sxs-lookup"><span data-stu-id="11c87-105">DESCRIPTION</span></span>
<span data-ttu-id="11c87-106">**AzureRmApiManagementTenantAccess** Cmdlet 會取得租使用者的租使用者存取設定。</span><span class="sxs-lookup"><span data-stu-id="11c87-106">The **Get-AzureRmApiManagementTenantAccess** cmdlet gets the tenant access configuration for a tenant.</span></span>

## <span data-ttu-id="11c87-107">示例</span><span class="sxs-lookup"><span data-stu-id="11c87-107">EXAMPLES</span></span>

### <span data-ttu-id="11c87-108">範例1：取得租使用者存取設定</span><span class="sxs-lookup"><span data-stu-id="11c87-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>Get-AzureRmApiManagementTenantAccess -Context $ApimContext
```

<span data-ttu-id="11c87-109">這個命令會取得指定內容的租使用者存取設定。</span><span class="sxs-lookup"><span data-stu-id="11c87-109">This command gets the tenant access configuration for the specified context.</span></span>

## <span data-ttu-id="11c87-110">參數</span><span class="sxs-lookup"><span data-stu-id="11c87-110">PARAMETERS</span></span>

### <span data-ttu-id="11c87-111">-內容</span><span class="sxs-lookup"><span data-stu-id="11c87-111">-Context</span></span>
<span data-ttu-id="11c87-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="11c87-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="11c87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11c87-113">-DefaultProfile</span></span>
<span data-ttu-id="11c87-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="11c87-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11c87-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11c87-115">CommonParameters</span></span>
<span data-ttu-id="11c87-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11c87-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11c87-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="11c87-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11c87-118">輸入</span><span class="sxs-lookup"><span data-stu-id="11c87-118">INPUTS</span></span>

## <span data-ttu-id="11c87-119">輸出</span><span class="sxs-lookup"><span data-stu-id="11c87-119">OUTPUTS</span></span>

### <span data-ttu-id="11c87-120">ServiceManagement. PsApiManagementAccessInformation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="11c87-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="11c87-121">筆記</span><span class="sxs-lookup"><span data-stu-id="11c87-121">NOTES</span></span>

## <span data-ttu-id="11c87-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="11c87-122">RELATED LINKS</span></span>

[<span data-ttu-id="11c87-123">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="11c87-123">Set-AzureRmApiManagementTenantAccess</span></span>](./Set-AzureRmApiManagementTenantAccess.md)


