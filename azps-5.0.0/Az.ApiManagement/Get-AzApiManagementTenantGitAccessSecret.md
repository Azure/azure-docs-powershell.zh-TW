---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccesssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccessSecret.md
ms.openlocfilehash: 51aea46ea65081dd63a3f9f9de4a3a80f4ae8986
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94288408"
---
# <span data-ttu-id="a9400-101">Get-AzApiManagementTenantGitAccessSecret</span><span class="sxs-lookup"><span data-stu-id="a9400-101">Get-AzApiManagementTenantGitAccessSecret</span></span>

## <span data-ttu-id="a9400-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9400-102">SYNOPSIS</span></span>
<span data-ttu-id="a9400-103">取得租使用者的 Git 存取設定鍵。</span><span class="sxs-lookup"><span data-stu-id="a9400-103">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="a9400-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9400-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccessSecret -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9400-105">說明</span><span class="sxs-lookup"><span data-stu-id="a9400-105">DESCRIPTION</span></span>
<span data-ttu-id="a9400-106">取得租使用者的 Git 存取設定鍵。</span><span class="sxs-lookup"><span data-stu-id="a9400-106">Gets the Git access configuration keys for a tenant.</span></span>

## <span data-ttu-id="a9400-107">示例</span><span class="sxs-lookup"><span data-stu-id="a9400-107">EXAMPLES</span></span>

### <span data-ttu-id="a9400-108">範例1：取得租使用者存取設定</span><span class="sxs-lookup"><span data-stu-id="a9400-108">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccessSecret -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="a9400-109">這個命令會取得指定內容的 Git 存取設定金鑰。</span><span class="sxs-lookup"><span data-stu-id="a9400-109">This command gets the Git access configuration keys for the specified context.</span></span>

## <span data-ttu-id="a9400-110">參數</span><span class="sxs-lookup"><span data-stu-id="a9400-110">PARAMETERS</span></span>

### <span data-ttu-id="a9400-111">-內容</span><span class="sxs-lookup"><span data-stu-id="a9400-111">-Context</span></span>
<span data-ttu-id="a9400-112">PsApiManagementCoNtext 的實例。</span><span class="sxs-lookup"><span data-stu-id="a9400-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a9400-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="a9400-113">This parameter is required.</span></span>

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

### <span data-ttu-id="a9400-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9400-114">-DefaultProfile</span></span>
<span data-ttu-id="a9400-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9400-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9400-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9400-116">CommonParameters</span></span>
<span data-ttu-id="a9400-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9400-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9400-118">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a9400-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9400-119">輸入</span><span class="sxs-lookup"><span data-stu-id="a9400-119">INPUTS</span></span>

### <span data-ttu-id="a9400-120">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a9400-120">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="a9400-121">輸出</span><span class="sxs-lookup"><span data-stu-id="a9400-121">OUTPUTS</span></span>

### <span data-ttu-id="a9400-122">ServiceManagement. PsApiManagementAccessInformation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="a9400-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="a9400-123">筆記</span><span class="sxs-lookup"><span data-stu-id="a9400-123">NOTES</span></span>

## <span data-ttu-id="a9400-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9400-124">RELATED LINKS</span></span>
