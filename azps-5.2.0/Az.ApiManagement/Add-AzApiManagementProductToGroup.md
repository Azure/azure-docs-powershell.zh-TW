---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: a92387392c540c75cfa96ecaf4c4acf026ade9f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98276015"
---
# <span data-ttu-id="8fff5-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="8fff5-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="8fff5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8fff5-102">SYNOPSIS</span></span>
<span data-ttu-id="8fff5-103">在群組中新增產品。</span><span class="sxs-lookup"><span data-stu-id="8fff5-103">Adds a product to a group.</span></span>

## <span data-ttu-id="8fff5-104">句法</span><span class="sxs-lookup"><span data-stu-id="8fff5-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fff5-105">說明</span><span class="sxs-lookup"><span data-stu-id="8fff5-105">DESCRIPTION</span></span>
<span data-ttu-id="8fff5-106">**載入 AzApiManagementProductToGroup** Cmdlet 會將產品新增至現有的群組。</span><span class="sxs-lookup"><span data-stu-id="8fff5-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="8fff5-107">換句話說，這個 Cmdlet 會將群組指派給產品。</span><span class="sxs-lookup"><span data-stu-id="8fff5-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="8fff5-108">示例</span><span class="sxs-lookup"><span data-stu-id="8fff5-108">EXAMPLES</span></span>

### <span data-ttu-id="8fff5-109">範例1：將產品新增至群組</span><span class="sxs-lookup"><span data-stu-id="8fff5-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="8fff5-110">這個命令會將產品新增至現有的群組。</span><span class="sxs-lookup"><span data-stu-id="8fff5-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="8fff5-111">參數</span><span class="sxs-lookup"><span data-stu-id="8fff5-111">PARAMETERS</span></span>

### <span data-ttu-id="8fff5-112">-內容</span><span class="sxs-lookup"><span data-stu-id="8fff5-112">-Context</span></span>
<span data-ttu-id="8fff5-113">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="8fff5-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="8fff5-114">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="8fff5-114">This parameter is required.</span></span>

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

### <span data-ttu-id="8fff5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fff5-115">-DefaultProfile</span></span>
<span data-ttu-id="8fff5-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8fff5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fff5-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="8fff5-117">-GroupId</span></span>
<span data-ttu-id="8fff5-118">指定群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="8fff5-118">Specifies the group ID.</span></span>
<span data-ttu-id="8fff5-119">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="8fff5-119">This parameter is required.</span></span>

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

### <span data-ttu-id="8fff5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8fff5-120">-PassThru</span></span>
<span data-ttu-id="8fff5-121">passthru</span><span class="sxs-lookup"><span data-stu-id="8fff5-121">passthru</span></span>

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

### <span data-ttu-id="8fff5-122">-產品識別碼</span><span class="sxs-lookup"><span data-stu-id="8fff5-122">-ProductId</span></span>
<span data-ttu-id="8fff5-123">指定產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="8fff5-123">Specifies the product ID.</span></span>
<span data-ttu-id="8fff5-124">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="8fff5-124">This parameter is required.</span></span>

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

### <span data-ttu-id="8fff5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fff5-125">CommonParameters</span></span>
<span data-ttu-id="8fff5-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8fff5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fff5-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8fff5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fff5-128">輸入</span><span class="sxs-lookup"><span data-stu-id="8fff5-128">INPUTS</span></span>

### <span data-ttu-id="8fff5-129">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="8fff5-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8fff5-130">System.object</span><span class="sxs-lookup"><span data-stu-id="8fff5-130">System.String</span></span>

### <span data-ttu-id="8fff5-131">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="8fff5-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8fff5-132">輸出</span><span class="sxs-lookup"><span data-stu-id="8fff5-132">OUTPUTS</span></span>

### <span data-ttu-id="8fff5-133">System.object</span><span class="sxs-lookup"><span data-stu-id="8fff5-133">System.Boolean</span></span>

## <span data-ttu-id="8fff5-134">筆記</span><span class="sxs-lookup"><span data-stu-id="8fff5-134">NOTES</span></span>

## <span data-ttu-id="8fff5-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="8fff5-135">RELATED LINKS</span></span>

[<span data-ttu-id="8fff5-136">移除-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="8fff5-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


