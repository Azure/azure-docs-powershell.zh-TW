---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
ms.openlocfilehash: 1bd1027c0d58f1ee38ca23c28b3021bdc2b95d19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445843"
---
# <span data-ttu-id="de1f8-101">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="de1f8-101">Add-AzureRmApiManagementProductToGroup</span></span>

## <span data-ttu-id="de1f8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="de1f8-102">SYNOPSIS</span></span>
<span data-ttu-id="de1f8-103">在群組中新增產品。</span><span class="sxs-lookup"><span data-stu-id="de1f8-103">Adds a product to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de1f8-104">句法</span><span class="sxs-lookup"><span data-stu-id="de1f8-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de1f8-105">說明</span><span class="sxs-lookup"><span data-stu-id="de1f8-105">DESCRIPTION</span></span>
<span data-ttu-id="de1f8-106">**載入 AzureRmApiManagementProductToGroup** Cmdlet 會將產品新增至現有的群組。</span><span class="sxs-lookup"><span data-stu-id="de1f8-106">The **Add-AzureRmApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="de1f8-107">換句話說，這個 Cmdlet 會將群組指派給產品。</span><span class="sxs-lookup"><span data-stu-id="de1f8-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="de1f8-108">示例</span><span class="sxs-lookup"><span data-stu-id="de1f8-108">EXAMPLES</span></span>

### <span data-ttu-id="de1f8-109">範例1：將產品新增至群組</span><span class="sxs-lookup"><span data-stu-id="de1f8-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="de1f8-110">這個命令會將產品新增至現有的群組。</span><span class="sxs-lookup"><span data-stu-id="de1f8-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="de1f8-111">參數</span><span class="sxs-lookup"><span data-stu-id="de1f8-111">PARAMETERS</span></span>

### <span data-ttu-id="de1f8-112">-內容</span><span class="sxs-lookup"><span data-stu-id="de1f8-112">-Context</span></span>
<span data-ttu-id="de1f8-113">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="de1f8-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="de1f8-114">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="de1f8-114">This parameter is required.</span></span>

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

### <span data-ttu-id="de1f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de1f8-115">-DefaultProfile</span></span>
<span data-ttu-id="de1f8-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="de1f8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de1f8-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="de1f8-117">-GroupId</span></span>
<span data-ttu-id="de1f8-118">指定群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="de1f8-118">Specifies the group ID.</span></span>
<span data-ttu-id="de1f8-119">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="de1f8-119">This parameter is required.</span></span>

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

### <span data-ttu-id="de1f8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de1f8-120">-PassThru</span></span>
<span data-ttu-id="de1f8-121">passthru</span><span class="sxs-lookup"><span data-stu-id="de1f8-121">passthru</span></span>

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

### <span data-ttu-id="de1f8-122">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="de1f8-122">-ProductId</span></span>
<span data-ttu-id="de1f8-123">指定產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="de1f8-123">Specifies the product ID.</span></span>
<span data-ttu-id="de1f8-124">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="de1f8-124">This parameter is required.</span></span>

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

### <span data-ttu-id="de1f8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de1f8-125">CommonParameters</span></span>
<span data-ttu-id="de1f8-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="de1f8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de1f8-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="de1f8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de1f8-128">輸入</span><span class="sxs-lookup"><span data-stu-id="de1f8-128">INPUTS</span></span>

### <span data-ttu-id="de1f8-129">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="de1f8-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="de1f8-130">System.object</span><span class="sxs-lookup"><span data-stu-id="de1f8-130">System.String</span></span>

### <span data-ttu-id="de1f8-131">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="de1f8-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="de1f8-132">輸出</span><span class="sxs-lookup"><span data-stu-id="de1f8-132">OUTPUTS</span></span>

### <span data-ttu-id="de1f8-133">System.object</span><span class="sxs-lookup"><span data-stu-id="de1f8-133">System.Boolean</span></span>

## <span data-ttu-id="de1f8-134">筆記</span><span class="sxs-lookup"><span data-stu-id="de1f8-134">NOTES</span></span>

## <span data-ttu-id="de1f8-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="de1f8-135">RELATED LINKS</span></span>

[<span data-ttu-id="de1f8-136">移除-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="de1f8-136">Remove-AzureRmApiManagementProductFromGroup</span></span>](./Remove-AzureRmApiManagementProductFromGroup.md)


