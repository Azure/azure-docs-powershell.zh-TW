---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 8C014335-9622-4F2E-A163-4B0C84531506
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementusertogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementUserToGroup.md
ms.openlocfilehash: 27e6be451d6141e322c47b2a84a28baf115839ef
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970706"
---
# <span data-ttu-id="f1b08-101">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="f1b08-101">Add-AzApiManagementUserToGroup</span></span>

## <span data-ttu-id="f1b08-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1b08-102">SYNOPSIS</span></span>
<span data-ttu-id="f1b08-103">將使用者新增至群組。</span><span class="sxs-lookup"><span data-stu-id="f1b08-103">Adds a user to a group.</span></span>

## <span data-ttu-id="f1b08-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1b08-104">SYNTAX</span></span>

```
Add-AzApiManagementUserToGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1b08-105">說明</span><span class="sxs-lookup"><span data-stu-id="f1b08-105">DESCRIPTION</span></span>
<span data-ttu-id="f1b08-106">**AzApiManagementUserToGroup** Cmdlet 會將使用者新增至群組。</span><span class="sxs-lookup"><span data-stu-id="f1b08-106">The **Add-AzApiManagementUserToGroup** cmdlet adds a user to a group.</span></span>

## <span data-ttu-id="f1b08-107">示例</span><span class="sxs-lookup"><span data-stu-id="f1b08-107">EXAMPLES</span></span>

### <span data-ttu-id="f1b08-108">範例1：將使用者新增至群組</span><span class="sxs-lookup"><span data-stu-id="f1b08-108">Example 1: Add a user to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementUserToGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="f1b08-109">這個命令會將現有的使用者新增至現有的群組。</span><span class="sxs-lookup"><span data-stu-id="f1b08-109">This command adds an existing user to an existing group.</span></span>

## <span data-ttu-id="f1b08-110">參數</span><span class="sxs-lookup"><span data-stu-id="f1b08-110">PARAMETERS</span></span>

### <span data-ttu-id="f1b08-111">-內容</span><span class="sxs-lookup"><span data-stu-id="f1b08-111">-Context</span></span>
<span data-ttu-id="f1b08-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="f1b08-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f1b08-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f1b08-113">This parameter is required.</span></span>

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

### <span data-ttu-id="f1b08-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1b08-114">-DefaultProfile</span></span>
<span data-ttu-id="f1b08-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1b08-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1b08-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="f1b08-116">-GroupId</span></span>
<span data-ttu-id="f1b08-117">指定群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="f1b08-117">Specifies the group ID.</span></span>
<span data-ttu-id="f1b08-118">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f1b08-118">This parameter is required.</span></span>

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

### <span data-ttu-id="f1b08-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1b08-119">-PassThru</span></span>
<span data-ttu-id="f1b08-120">passthru</span><span class="sxs-lookup"><span data-stu-id="f1b08-120">passthru</span></span>

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

### <span data-ttu-id="f1b08-121">-UserId</span><span class="sxs-lookup"><span data-stu-id="f1b08-121">-UserId</span></span>
<span data-ttu-id="f1b08-122">指定使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="f1b08-122">Specifies the user ID.</span></span>
<span data-ttu-id="f1b08-123">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f1b08-123">This parameter is required.</span></span>

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

### <span data-ttu-id="f1b08-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1b08-124">CommonParameters</span></span>
<span data-ttu-id="f1b08-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1b08-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1b08-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f1b08-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1b08-127">輸入</span><span class="sxs-lookup"><span data-stu-id="f1b08-127">INPUTS</span></span>

### <span data-ttu-id="f1b08-128">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="f1b08-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f1b08-129">System.object</span><span class="sxs-lookup"><span data-stu-id="f1b08-129">System.String</span></span>

### <span data-ttu-id="f1b08-130">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="f1b08-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f1b08-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f1b08-131">OUTPUTS</span></span>

### <span data-ttu-id="f1b08-132">System.object</span><span class="sxs-lookup"><span data-stu-id="f1b08-132">System.Boolean</span></span>

## <span data-ttu-id="f1b08-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f1b08-133">NOTES</span></span>

## <span data-ttu-id="f1b08-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1b08-134">RELATED LINKS</span></span>

[<span data-ttu-id="f1b08-135">AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f1b08-135">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)

[<span data-ttu-id="f1b08-136">移除-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="f1b08-136">Remove-AzApiManagementUserFromGroup</span></span>](./Remove-AzApiManagementUserFromGroup.md)


