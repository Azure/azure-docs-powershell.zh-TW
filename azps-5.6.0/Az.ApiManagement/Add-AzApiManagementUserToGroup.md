---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: a56acc56bc100365f999ef1ca9a5f42f53b36096
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912946"
---
# <span data-ttu-id="cd6b4-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="cd6b4-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="cd6b4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="cd6b4-102">SYNOPSIS</span></span>
<span data-ttu-id="cd6b4-103">將使用者新增到群組。</span><span class="sxs-lookup"><span data-stu-id="cd6b4-103">Adds a user to a group.</span></span>

## <span data-ttu-id="cd6b4-104">語法</span><span class="sxs-lookup"><span data-stu-id="cd6b4-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd6b4-105">描述</span><span class="sxs-lookup"><span data-stu-id="cd6b4-105">DESCRIPTION</span></span>
<span data-ttu-id="cd6b4-106">**Add-AzApiManagementUserToGroup** Cmdlet 會將使用者新增到群組。</span><span class="sxs-lookup"><span data-stu-id="cd6b4-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="cd6b4-107">例子</span><span class="sxs-lookup"><span data-stu-id="cd6b4-107">EXAMPLES</span></span>

### <span data-ttu-id="cd6b4-108">範例 1：新增使用者至群組</span><span class="sxs-lookup"><span data-stu-id="cd6b4-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="cd6b4-109">此命令會將現有使用者新增到現有的群組。</span><span class="sxs-lookup"><span data-stu-id="cd6b4-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="cd6b4-110">參數</span><span class="sxs-lookup"><span data-stu-id="cd6b4-110">PARAMETERS</span></span>

### <span data-ttu-id="cd6b4-111">-內容</span><span class="sxs-lookup"><span data-stu-id="cd6b4-111">-Context</span></span>
<span data-ttu-id="cd6b4-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="cd6b4-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="cd6b4-113">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="cd6b4-113">This parameter is required.</span></span>

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

### <span data-ttu-id="cd6b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd6b4-114">-DefaultProfile</span></span>
<span data-ttu-id="cd6b4-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="cd6b4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd6b4-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="cd6b4-116">-GroupId</span></span>
<span data-ttu-id="cd6b4-117">指定群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd6b4-117">Specifies the group ID.</span></span>
<span data-ttu-id="cd6b4-118">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="cd6b4-118">This parameter is required.</span></span>

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

### <span data-ttu-id="cd6b4-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd6b4-119">-PassThru</span></span>
<span data-ttu-id="cd6b4-120">Passthru</span><span class="sxs-lookup"><span data-stu-id="cd6b4-120">passthru</span></span>

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

### <span data-ttu-id="cd6b4-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="cd6b4-121">-UserId</span></span>
<span data-ttu-id="cd6b4-122">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="cd6b4-122">Specifies the user ID.</span></span>
<span data-ttu-id="cd6b4-123">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="cd6b4-123">This parameter is required.</span></span>

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

### <span data-ttu-id="cd6b4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd6b4-124">CommonParameters</span></span>
<span data-ttu-id="cd6b4-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="cd6b4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd6b4-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd6b4-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd6b4-127">輸入</span><span class="sxs-lookup"><span data-stu-id="cd6b4-127">INPUTS</span></span>

### <span data-ttu-id="cd6b4-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="cd6b4-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cd6b4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="cd6b4-129">System.String</span></span>

### <span data-ttu-id="cd6b4-130">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cd6b4-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cd6b4-131">輸出</span><span class="sxs-lookup"><span data-stu-id="cd6b4-131">OUTPUTS</span></span>

### <span data-ttu-id="cd6b4-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cd6b4-132">System.Boolean</span></span>

## <span data-ttu-id="cd6b4-133">筆記</span><span class="sxs-lookup"><span data-stu-id="cd6b4-133">NOTES</span></span>

## <span data-ttu-id="cd6b4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="cd6b4-134">RELATED LINKS</span></span>

[<span data-ttu-id="cd6b4-135">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="cd6b4-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="cd6b4-136">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="cd6b4-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


