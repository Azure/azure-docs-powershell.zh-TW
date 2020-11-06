---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 2fe14349b179634bf93050840271d4d4b6905b3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611606"
---
# <span data-ttu-id="96ce8-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="96ce8-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="96ce8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="96ce8-102">SYNOPSIS</span></span>
<span data-ttu-id="96ce8-103">取得租使用者的 Git 存取設定。</span><span class="sxs-lookup"><span data-stu-id="96ce8-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="96ce8-104">句法</span><span class="sxs-lookup"><span data-stu-id="96ce8-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96ce8-105">說明</span><span class="sxs-lookup"><span data-stu-id="96ce8-105">DESCRIPTION</span></span>
<span data-ttu-id="96ce8-106">**AzApiManagementTenantGitAccess** Cmdlet 會取得租使用者的 Git 存取設定。</span><span class="sxs-lookup"><span data-stu-id="96ce8-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="96ce8-107">示例</span><span class="sxs-lookup"><span data-stu-id="96ce8-107">EXAMPLES</span></span>

### <span data-ttu-id="96ce8-108">範例1：取得租使用者存取設定</span><span class="sxs-lookup"><span data-stu-id="96ce8-108">Example 1: Get tenant access configuration</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

<span data-ttu-id="96ce8-109">這個命令會取得指定內容的 Git 存取設定。</span><span class="sxs-lookup"><span data-stu-id="96ce8-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="96ce8-110">參數</span><span class="sxs-lookup"><span data-stu-id="96ce8-110">PARAMETERS</span></span>

### <span data-ttu-id="96ce8-111">-內容</span><span class="sxs-lookup"><span data-stu-id="96ce8-111">-Context</span></span>
<span data-ttu-id="96ce8-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="96ce8-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="96ce8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96ce8-113">-DefaultProfile</span></span>
<span data-ttu-id="96ce8-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="96ce8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96ce8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96ce8-115">CommonParameters</span></span>
<span data-ttu-id="96ce8-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="96ce8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96ce8-117">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="96ce8-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96ce8-118">輸入</span><span class="sxs-lookup"><span data-stu-id="96ce8-118">INPUTS</span></span>

### <span data-ttu-id="96ce8-119">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="96ce8-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="96ce8-120">輸出</span><span class="sxs-lookup"><span data-stu-id="96ce8-120">OUTPUTS</span></span>

### <span data-ttu-id="96ce8-121">ServiceManagement. PsApiManagementAccessInformation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="96ce8-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="96ce8-122">筆記</span><span class="sxs-lookup"><span data-stu-id="96ce8-122">NOTES</span></span>

## <span data-ttu-id="96ce8-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="96ce8-123">RELATED LINKS</span></span>
