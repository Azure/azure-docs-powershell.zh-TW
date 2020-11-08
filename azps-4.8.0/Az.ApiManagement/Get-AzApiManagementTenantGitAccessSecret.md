---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 51aea46ea65081dd63a3f9f9de4a3a80f4ae8986
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971570"
---
# <span data-ttu-id="42d29-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="42d29-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="42d29-102">摘要</span><span class="sxs-lookup"><span data-stu-id="42d29-102">SYNOPSIS</span></span>
<span data-ttu-id="42d29-103">取得租使用者的 Git 存取設定鍵。</span><span class="sxs-lookup"><span data-stu-id="42d29-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="42d29-104">句法</span><span class="sxs-lookup"><span data-stu-id="42d29-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42d29-105">說明</span><span class="sxs-lookup"><span data-stu-id="42d29-105">DESCRIPTION</span></span>
<span data-ttu-id="42d29-106">取得租使用者的 Git 存取設定鍵。</span><span class="sxs-lookup"><span data-stu-id="42d29-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="42d29-107">示例</span><span class="sxs-lookup"><span data-stu-id="42d29-107">EXAMPLES</span></span>

### <span data-ttu-id="42d29-108">範例1：取得租使用者存取設定</span><span class="sxs-lookup"><span data-stu-id="42d29-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="42d29-109">這個命令會取得指定內容的 Git 存取設定金鑰。</span><span class="sxs-lookup"><span data-stu-id="42d29-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="42d29-110">參數</span><span class="sxs-lookup"><span data-stu-id="42d29-110">PARAMETERS</span></span>

### <span data-ttu-id="42d29-111">-內容</span><span class="sxs-lookup"><span data-stu-id="42d29-111">-Context</span></span>
<span data-ttu-id="42d29-112">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="42d29-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="42d29-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="42d29-113">This parameter is required.</span></span>

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

### <span data-ttu-id="42d29-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d29-114">-DefaultProfile</span></span>
<span data-ttu-id="42d29-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="42d29-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42d29-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d29-116">CommonParameters</span></span>
<span data-ttu-id="42d29-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="42d29-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d29-118">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="42d29-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d29-119">輸入</span><span class="sxs-lookup"><span data-stu-id="42d29-119">INPUTS</span></span>

### <span data-ttu-id="42d29-120">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="42d29-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="42d29-121">輸出</span><span class="sxs-lookup"><span data-stu-id="42d29-121">OUTPUTS</span></span>

### <span data-ttu-id="42d29-122">ServiceManagement. PsApiManagementAccessInformation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="42d29-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="42d29-123">筆記</span><span class="sxs-lookup"><span data-stu-id="42d29-123">NOTES</span></span>

## <span data-ttu-id="42d29-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="42d29-124">RELATED LINKS</span></span>
