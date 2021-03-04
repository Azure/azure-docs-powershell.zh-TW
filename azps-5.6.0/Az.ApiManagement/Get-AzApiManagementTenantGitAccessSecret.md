---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 471c861e8601317daf1e12de3a292d84bfce416e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915673"
---
# <span data-ttu-id="d43aa-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="d43aa-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="d43aa-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d43aa-102">SYNOPSIS</span></span>
<span data-ttu-id="d43aa-103">取得租使用者 Git 存取組組鍵。</span><span class="sxs-lookup"><span data-stu-id="d43aa-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="d43aa-104">語法</span><span class="sxs-lookup"><span data-stu-id="d43aa-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d43aa-105">描述</span><span class="sxs-lookup"><span data-stu-id="d43aa-105">DESCRIPTION</span></span>
<span data-ttu-id="d43aa-106">取得租使用者 Git 存取組組鍵。</span><span class="sxs-lookup"><span data-stu-id="d43aa-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="d43aa-107">例子</span><span class="sxs-lookup"><span data-stu-id="d43aa-107">EXAMPLES</span></span>

### <span data-ttu-id="d43aa-108">範例 1：取得租使用者存取組</span><span class="sxs-lookup"><span data-stu-id="d43aa-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="d43aa-109">此命令會取得指定上下文的 Git 訪問組組鍵。</span><span class="sxs-lookup"><span data-stu-id="d43aa-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="d43aa-110">參數</span><span class="sxs-lookup"><span data-stu-id="d43aa-110">PARAMETERS</span></span>

### <span data-ttu-id="d43aa-111">-內容</span><span class="sxs-lookup"><span data-stu-id="d43aa-111">-Context</span></span>
<span data-ttu-id="d43aa-112">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="d43aa-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d43aa-113">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="d43aa-113">This parameter is required.</span></span>

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

### <span data-ttu-id="d43aa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d43aa-114">-DefaultProfile</span></span>
<span data-ttu-id="d43aa-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d43aa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d43aa-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d43aa-116">CommonParameters</span></span>
<span data-ttu-id="d43aa-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d43aa-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d43aa-118">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d43aa-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d43aa-119">輸入</span><span class="sxs-lookup"><span data-stu-id="d43aa-119">INPUTS</span></span>

### <span data-ttu-id="d43aa-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="d43aa-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="d43aa-121">輸出</span><span class="sxs-lookup"><span data-stu-id="d43aa-121">OUTPUTS</span></span>

### <span data-ttu-id="d43aa-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="d43aa-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="d43aa-123">筆記</span><span class="sxs-lookup"><span data-stu-id="d43aa-123">NOTES</span></span>

## <span data-ttu-id="d43aa-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="d43aa-124">RELATED LINKS</span></span>
