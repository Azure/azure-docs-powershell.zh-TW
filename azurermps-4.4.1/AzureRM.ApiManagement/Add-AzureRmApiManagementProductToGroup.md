---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
ms.openlocfilehash: b4e1a029eca4e7eda48f44d85292639767eaf845
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452639"
---
# <span data-ttu-id="f5aab-101">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="f5aab-101">Add-AzureRmApiManagementProductToGroup</span></span>

## <span data-ttu-id="f5aab-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5aab-102">SYNOPSIS</span></span>
<span data-ttu-id="f5aab-103">在群組中新增產品。</span><span class="sxs-lookup"><span data-stu-id="f5aab-103">Adds a product to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5aab-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5aab-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5aab-105">說明</span><span class="sxs-lookup"><span data-stu-id="f5aab-105">DESCRIPTION</span></span>
<span data-ttu-id="f5aab-106">**載入 AzureRmApiManagementProductToGroup** Cmdlet 會將產品新增至現有的群組。</span><span class="sxs-lookup"><span data-stu-id="f5aab-106">The **Add-AzureRmApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="f5aab-107">換句話說，這個 Cmdlet 會將群組指派給產品。</span><span class="sxs-lookup"><span data-stu-id="f5aab-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="f5aab-108">示例</span><span class="sxs-lookup"><span data-stu-id="f5aab-108">EXAMPLES</span></span>

### <span data-ttu-id="f5aab-109">範例1：將產品新增至群組</span><span class="sxs-lookup"><span data-stu-id="f5aab-109">Example 1: Add a product to a group</span></span>
```
PS C:\>Add-AzureRmApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="f5aab-110">這個命令會將產品新增至現有的群組。</span><span class="sxs-lookup"><span data-stu-id="f5aab-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="f5aab-111">參數</span><span class="sxs-lookup"><span data-stu-id="f5aab-111">PARAMETERS</span></span>

### <span data-ttu-id="f5aab-112">-內容</span><span class="sxs-lookup"><span data-stu-id="f5aab-112">-Context</span></span>
<span data-ttu-id="f5aab-113">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="f5aab-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f5aab-114">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f5aab-114">This parameter is required.</span></span>

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

### <span data-ttu-id="f5aab-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="f5aab-115">-GroupId</span></span>
<span data-ttu-id="f5aab-116">指定群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="f5aab-116">Specifies the group ID.</span></span>
<span data-ttu-id="f5aab-117">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f5aab-117">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5aab-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5aab-118">-PassThru</span></span>
<span data-ttu-id="f5aab-119">passthru</span><span class="sxs-lookup"><span data-stu-id="f5aab-119">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5aab-120">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="f5aab-120">-ProductId</span></span>
<span data-ttu-id="f5aab-121">指定產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="f5aab-121">Specifies the product ID.</span></span>
<span data-ttu-id="f5aab-122">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f5aab-122">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5aab-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5aab-123">-DefaultProfile</span></span>
<span data-ttu-id="f5aab-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5aab-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5aab-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5aab-125">CommonParameters</span></span>
<span data-ttu-id="f5aab-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5aab-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5aab-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f5aab-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5aab-128">輸入</span><span class="sxs-lookup"><span data-stu-id="f5aab-128">INPUTS</span></span>

## <span data-ttu-id="f5aab-129">輸出</span><span class="sxs-lookup"><span data-stu-id="f5aab-129">OUTPUTS</span></span>

### <span data-ttu-id="f5aab-130">布林值</span><span class="sxs-lookup"><span data-stu-id="f5aab-130">Boolean</span></span>

## <span data-ttu-id="f5aab-131">筆記</span><span class="sxs-lookup"><span data-stu-id="f5aab-131">NOTES</span></span>

## <span data-ttu-id="f5aab-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5aab-132">RELATED LINKS</span></span>

[<span data-ttu-id="f5aab-133">移除-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="f5aab-133">Remove-AzureRmApiManagementProductFromGroup</span></span>](./Remove-AzureRmApiManagementProductFromGroup.md)


