---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 3338ae75406cc7c9253b21a52726f283f19d4ad7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614028"
---
# <span data-ttu-id="bf09c-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="bf09c-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="bf09c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bf09c-102">SYNOPSIS</span></span>
<span data-ttu-id="bf09c-103">取得租使用者的 Git 存取設定。</span><span class="sxs-lookup"><span data-stu-id="bf09c-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="bf09c-104">句法</span><span class="sxs-lookup"><span data-stu-id="bf09c-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf09c-105">說明</span><span class="sxs-lookup"><span data-stu-id="bf09c-105">DESCRIPTION</span></span>
<span data-ttu-id="bf09c-106">**AzApiManagementTenantGitAccess** Cmdlet 會取得租使用者的 Git 存取設定。</span><span class="sxs-lookup"><span data-stu-id="bf09c-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="bf09c-107">示例</span><span class="sxs-lookup"><span data-stu-id="bf09c-107">EXAMPLES</span></span>

### <span data-ttu-id="bf09c-108">範例1：取得租使用者存取設定</span><span class="sxs-lookup"><span data-stu-id="bf09c-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="bf09c-109">這個命令會取得指定內容的 Git 存取設定。</span><span class="sxs-lookup"><span data-stu-id="bf09c-109">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="bf09c-110">參數</span><span class="sxs-lookup"><span data-stu-id="bf09c-110">PARAMETERS</span></span>

### <span data-ttu-id="bf09c-111">-內容</span><span class="sxs-lookup"><span data-stu-id="bf09c-111">-Context</span></span>
<span data-ttu-id="bf09c-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="bf09c-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bf09c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf09c-113">-DefaultProfile</span></span>
<span data-ttu-id="bf09c-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bf09c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf09c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf09c-115">CommonParameters</span></span>
<span data-ttu-id="bf09c-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bf09c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf09c-117">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bf09c-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf09c-118">輸入</span><span class="sxs-lookup"><span data-stu-id="bf09c-118">INPUTS</span></span>

### <span data-ttu-id="bf09c-119">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="bf09c-119">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="bf09c-120">輸出</span><span class="sxs-lookup"><span data-stu-id="bf09c-120">OUTPUTS</span></span>

### <span data-ttu-id="bf09c-121">ServiceManagement. PsApiManagementAccessInformation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="bf09c-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="bf09c-122">筆記</span><span class="sxs-lookup"><span data-stu-id="bf09c-122">NOTES</span></span>

## <span data-ttu-id="bf09c-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="bf09c-123">RELATED LINKS</span></span>
