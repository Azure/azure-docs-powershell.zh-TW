---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F01F494-CD1D-483A-9E57-BF693B1F2FC1
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementtenantgitaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementTenantGitAccess.md
ms.openlocfilehash: 0a3d2aeb8c90377f9c7e81ef6a25cef49780e410
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139392"
---
# <span data-ttu-id="4c369-101">Get-AzApiManagementTenantGitAccess</span><span class="sxs-lookup"><span data-stu-id="4c369-101">Get-AzApiManagementTenantGitAccess</span></span>

## <span data-ttu-id="4c369-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c369-102">SYNOPSIS</span></span>
<span data-ttu-id="4c369-103">取得租使用者的 Git 存取設定。</span><span class="sxs-lookup"><span data-stu-id="4c369-103">Gets the Git access configuration for a tenant.</span></span>

## <span data-ttu-id="4c369-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c369-104">SYNTAX</span></span>

```
Get-AzApiManagementTenantGitAccess -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c369-105">說明</span><span class="sxs-lookup"><span data-stu-id="4c369-105">DESCRIPTION</span></span>
<span data-ttu-id="4c369-106">**AzApiManagementTenantGitAccess** Cmdlet 會取得租使用者的 Git 存取設定。</span><span class="sxs-lookup"><span data-stu-id="4c369-106">The **Get-AzApiManagementTenantGitAccess** cmdlet gets the Git access configuration for a tenant.</span></span>
<span data-ttu-id="4c369-107">[結果詳細資料] 中不會包含按鍵。</span><span class="sxs-lookup"><span data-stu-id="4c369-107">Keys will not be included into result details.</span></span> <span data-ttu-id="4c369-108">若要取得用戶端密碼，請使用 **AzApiManagementTenantGitAccessSecret** 。</span><span class="sxs-lookup"><span data-stu-id="4c369-108">To get client secret, use **Get-AzApiManagementTenantGitAccessSecret**.</span></span>

## <span data-ttu-id="4c369-109">示例</span><span class="sxs-lookup"><span data-stu-id="4c369-109">EXAMPLES</span></span>

### <span data-ttu-id="4c369-110">範例1：取得租使用者存取設定</span><span class="sxs-lookup"><span data-stu-id="4c369-110">Example 1: Get tenant access configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementTenantGitAccess -Context $apimContext
```

```
Enabled Id  PrimaryKey                                                                               SecondaryKey
------- --  ----------                                                                               ------------
   True git GrPksEiunqn1BgprRvWIZZxUuaRl9vdz0ZFjVBxxx==             OR4wVD//HzaE4Okb6aSdG9zy0O6kHhmfIJBaL9Zwu+Mxxxf9R2ydOslIw==
```

<span data-ttu-id="4c369-111">這個命令會取得指定內容的 Git 存取設定。</span><span class="sxs-lookup"><span data-stu-id="4c369-111">This command gets the Git access configuration for the specified context.</span></span>

## <span data-ttu-id="4c369-112">參數</span><span class="sxs-lookup"><span data-stu-id="4c369-112">PARAMETERS</span></span>

### <span data-ttu-id="4c369-113">-內容</span><span class="sxs-lookup"><span data-stu-id="4c369-113">-Context</span></span>
<span data-ttu-id="4c369-114">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="4c369-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4c369-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c369-115">-DefaultProfile</span></span>
<span data-ttu-id="4c369-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4c369-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c369-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c369-117">CommonParameters</span></span>
<span data-ttu-id="4c369-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c369-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c369-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4c369-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c369-120">輸入</span><span class="sxs-lookup"><span data-stu-id="4c369-120">INPUTS</span></span>

### <span data-ttu-id="4c369-121">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="4c369-121">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="4c369-122">輸出</span><span class="sxs-lookup"><span data-stu-id="4c369-122">OUTPUTS</span></span>

### <span data-ttu-id="4c369-123">ServiceManagement. PsApiManagementAccessInformation （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="4c369-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="4c369-124">筆記</span><span class="sxs-lookup"><span data-stu-id="4c369-124">NOTES</span></span>

## <span data-ttu-id="4c369-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c369-125">RELATED LINKS</span></span>