---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementUserToGroup.md
ms.openlocfilehash: abb86f40c9ac4a2ca04e0f14500df6c39e550dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452915"
---
# <span data-ttu-id="e2196-101">Add-AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="e2196-101">Add-AzureRmApiManagementUserToGroup</span></span>

## <span data-ttu-id="e2196-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e2196-102">SYNOPSIS</span></span>
<span data-ttu-id="e2196-103">將使用者新增至群組。</span><span class="sxs-lookup"><span data-stu-id="e2196-103">Adds a user to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2196-104">句法</span><span class="sxs-lookup"><span data-stu-id="e2196-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2196-105">說明</span><span class="sxs-lookup"><span data-stu-id="e2196-105">DESCRIPTION</span></span>
<span data-ttu-id="e2196-106">**AzureRmApiManagementUserToGroup** Cmdlet 會將使用者新增至群組。</span><span class="sxs-lookup"><span data-stu-id="e2196-106">The **Add-AzureRmApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="e2196-107">示例</span><span class="sxs-lookup"><span data-stu-id="e2196-107">EXAMPLES</span></span>

### <span data-ttu-id="e2196-108">範例1：將使用者新增至群組</span><span class="sxs-lookup"><span data-stu-id="e2196-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="e2196-109">這個命令會將現有的使用者新增至現有的群組。</span><span class="sxs-lookup"><span data-stu-id="e2196-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="e2196-110">參數</span><span class="sxs-lookup"><span data-stu-id="e2196-110">PARAMETERS</span></span>

### <span data-ttu-id="e2196-111">-內容</span><span class="sxs-lookup"><span data-stu-id="e2196-111">-Context</span></span>
<span data-ttu-id="e2196-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="e2196-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="e2196-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="e2196-113">This parameter is required.</span></span>

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

### <span data-ttu-id="e2196-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2196-114">-DefaultProfile</span></span>
<span data-ttu-id="e2196-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e2196-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2196-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="e2196-116">-GroupId</span></span>
<span data-ttu-id="e2196-117">指定群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="e2196-117">Specifies the group ID.</span></span>
<span data-ttu-id="e2196-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="e2196-118">This parameter is required.</span></span>

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

### <span data-ttu-id="e2196-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e2196-119">-PassThru</span></span>
<span data-ttu-id="e2196-120">passthru</span><span class="sxs-lookup"><span data-stu-id="e2196-120">passthru</span></span>

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

### <span data-ttu-id="e2196-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="e2196-121">-UserId</span></span>
<span data-ttu-id="e2196-122">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="e2196-122">Specifies the user ID.</span></span>
<span data-ttu-id="e2196-123">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="e2196-123">This parameter is required.</span></span>

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

### <span data-ttu-id="e2196-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2196-124">CommonParameters</span></span>
<span data-ttu-id="e2196-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e2196-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2196-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e2196-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2196-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e2196-127">INPUTS</span></span>

### <span data-ttu-id="e2196-128">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="e2196-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e2196-129">System.object</span><span class="sxs-lookup"><span data-stu-id="e2196-129">System.String</span></span>

### <span data-ttu-id="e2196-130">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="e2196-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e2196-131">輸出</span><span class="sxs-lookup"><span data-stu-id="e2196-131">OUTPUTS</span></span>

### <span data-ttu-id="e2196-132">System.object</span><span class="sxs-lookup"><span data-stu-id="e2196-132">System.Boolean</span></span>

## <span data-ttu-id="e2196-133">筆記</span><span class="sxs-lookup"><span data-stu-id="e2196-133">NOTES</span></span>

## <span data-ttu-id="e2196-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="e2196-134">RELATED LINKS</span></span>

[<span data-ttu-id="e2196-135">AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="e2196-135">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="e2196-136">移除-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="e2196-136">Remove-AzureRmApiManagementUserFromGroup</span></span>](./Remove-AzureRmApiManagementUserFromGroup.md)


