---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 03073dc6116595c93b2c25d30b38c5467482903c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916795"
---
# <span data-ttu-id="d2a95-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="d2a95-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="d2a95-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d2a95-102">SYNOPSIS</span></span>
<span data-ttu-id="d2a95-103">從群組移除使用者。</span><span class="sxs-lookup"><span data-stu-id="d2a95-103">Removes a user from a group.</span></span>

## <span data-ttu-id="d2a95-104">語法</span><span class="sxs-lookup"><span data-stu-id="d2a95-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2a95-105">描述</span><span class="sxs-lookup"><span data-stu-id="d2a95-105">DESCRIPTION</span></span>
<span data-ttu-id="d2a95-106">**Remove-AzApiManagementUserFromGroup** Cmdlet 會從現有的群組移除使用者。</span><span class="sxs-lookup"><span data-stu-id="d2a95-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="d2a95-107">例子</span><span class="sxs-lookup"><span data-stu-id="d2a95-107">EXAMPLES</span></span>

### <span data-ttu-id="d2a95-108">範例 1：從群組移除使用者</span><span class="sxs-lookup"><span data-stu-id="d2a95-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="d2a95-109">此命令會從群組移除使用者。</span><span class="sxs-lookup"><span data-stu-id="d2a95-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="d2a95-110">參數</span><span class="sxs-lookup"><span data-stu-id="d2a95-110">PARAMETERS</span></span>

### <span data-ttu-id="d2a95-111">-內容</span><span class="sxs-lookup"><span data-stu-id="d2a95-111">-Context</span></span>
<span data-ttu-id="d2a95-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="d2a95-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="d2a95-113">此參數為必填項。</span><span class="sxs-lookup"><span data-stu-id="d2a95-113">This parameter is required.</span></span>

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

### <span data-ttu-id="d2a95-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2a95-114">-DefaultProfile</span></span>
<span data-ttu-id="d2a95-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d2a95-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2a95-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="d2a95-116">-GroupId</span></span>
<span data-ttu-id="d2a95-117">指定要移除使用者的群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2a95-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="d2a95-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d2a95-118">-PassThru</span></span>
<span data-ttu-id="d2a95-119">表示此 Cmdlet 會$True值 ，否則會$False值。</span><span class="sxs-lookup"><span data-stu-id="d2a95-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="d2a95-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="d2a95-120">-UserId</span></span>
<span data-ttu-id="d2a95-121">指定要從群組移除的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="d2a95-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="d2a95-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2a95-122">CommonParameters</span></span>
<span data-ttu-id="d2a95-123">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d2a95-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2a95-124">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2a95-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2a95-125">輸入</span><span class="sxs-lookup"><span data-stu-id="d2a95-125">INPUTS</span></span>

### <span data-ttu-id="d2a95-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.models.PsApiManagementCoNtext</span><span class="sxs-lookup"><span data-stu-id="d2a95-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d2a95-127">System.String</span><span class="sxs-lookup"><span data-stu-id="d2a95-127">System.String</span></span>

### <span data-ttu-id="d2a95-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d2a95-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d2a95-129">輸出</span><span class="sxs-lookup"><span data-stu-id="d2a95-129">OUTPUTS</span></span>

### <span data-ttu-id="d2a95-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d2a95-130">System.Boolean</span></span>

## <span data-ttu-id="d2a95-131">筆記</span><span class="sxs-lookup"><span data-stu-id="d2a95-131">NOTES</span></span>

## <span data-ttu-id="d2a95-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="d2a95-132">RELATED LINKS</span></span>

[<span data-ttu-id="d2a95-133">Add-AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="d2a95-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="d2a95-134">Get-AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="d2a95-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


