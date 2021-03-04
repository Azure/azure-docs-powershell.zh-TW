---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 29e15515dfb5c8db53255cd283573fec11239940
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915677"
---
# <span data-ttu-id="f60c1-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="f60c1-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="f60c1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f60c1-102">SYNOPSIS</span></span>
<span data-ttu-id="f60c1-103">取得租使用者 Git 存取組。</span><span class="sxs-lookup"><span data-stu-id="f60c1-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="f60c1-104">語法</span><span class="sxs-lookup"><span data-stu-id="f60c1-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f60c1-105">描述</span><span class="sxs-lookup"><span data-stu-id="f60c1-105">DESCRIPTION</span></span>
<span data-ttu-id="f60c1-106">**Get-AzApiManagementTenantGitAccess** Cmdlet 會取得租使用者 Git 存取組式。</span><span class="sxs-lookup"><span data-stu-id="f60c1-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>
<span data-ttu-id="f60c1-107">按鍵不會包含在結果詳細資料中。</span><span class="sxs-lookup"><span data-stu-id="f60c1-107">Keys will not be included into result details.</span></span> <span data-ttu-id="f60c1-108">若要取得用戶端機密，請使用 **Get-AzApiManagementTenantGitAccessSecret。**</span><span class="sxs-lookup"><span data-stu-id="f60c1-108">To get client secret, use **Get-AzApiManagementTenantGitAccessSecret**.</span></span>

## <span data-ttu-id="f60c1-109">例子</span><span class="sxs-lookup"><span data-stu-id="f60c1-109">EXAMPLES</span></span>

### <span data-ttu-id="f60c1-110">範例 1：取得租使用者存取組</span><span class="sxs-lookup"><span data-stu-id="f60c1-110">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="f60c1-111">此命令會取得指定上下文的 Git 存取組組。</span><span class="sxs-lookup"><span data-stu-id="f60c1-111">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="f60c1-112">參數</span><span class="sxs-lookup"><span data-stu-id="f60c1-112">PARAMETERS</span></span>

### <span data-ttu-id="f60c1-113">-內容</span><span class="sxs-lookup"><span data-stu-id="f60c1-113">-Context</span></span>
<span data-ttu-id="f60c1-114">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="f60c1-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f60c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f60c1-115">-DefaultProfile</span></span>
<span data-ttu-id="f60c1-116">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f60c1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f60c1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f60c1-117">CommonParameters</span></span>
<span data-ttu-id="f60c1-118">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f60c1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f60c1-119">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f60c1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f60c1-120">輸入</span><span class="sxs-lookup"><span data-stu-id="f60c1-120">INPUTS</span></span>

### <span data-ttu-id="f60c1-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="f60c1-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="f60c1-122">輸出</span><span class="sxs-lookup"><span data-stu-id="f60c1-122">OUTPUTS</span></span>

### <span data-ttu-id="f60c1-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="f60c1-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="f60c1-124">筆記</span><span class="sxs-lookup"><span data-stu-id="f60c1-124">NOTES</span></span>

## <span data-ttu-id="f60c1-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="f60c1-125">RELATED LINKS</span></span>
