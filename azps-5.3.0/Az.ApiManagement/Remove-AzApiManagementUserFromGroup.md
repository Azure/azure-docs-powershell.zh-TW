---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementuserfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementUserFromGroup.md
ms.openlocfilehash: 220af172efa397de2fc0fafa7597c2b6e29dae60
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287699"
---
# <span data-ttu-id="1fe8e-101">Remove-AzApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="1fe8e-101">Remove-AzApiManagementUserFromGroup</span></span>

## <span data-ttu-id="1fe8e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1fe8e-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe8e-103">從群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="1fe8e-103">Removes a user from a group.</span></span>

## <span data-ttu-id="1fe8e-104">句法</span><span class="sxs-lookup"><span data-stu-id="1fe8e-104">SYNTAX</span></span>

```
Remove-AzApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1fe8e-105">說明</span><span class="sxs-lookup"><span data-stu-id="1fe8e-105">DESCRIPTION</span></span>
<span data-ttu-id="1fe8e-106">**AzApiManagementUserFromGroup** Cmdlet 會從現有的群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="1fe8e-106">The **Remove-AzApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="1fe8e-107">示例</span><span class="sxs-lookup"><span data-stu-id="1fe8e-107">EXAMPLES</span></span>

### <span data-ttu-id="1fe8e-108">範例1：從群組中移除使用者</span><span class="sxs-lookup"><span data-stu-id="1fe8e-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="1fe8e-109">這個命令會從群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="1fe8e-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="1fe8e-110">參數</span><span class="sxs-lookup"><span data-stu-id="1fe8e-110">PARAMETERS</span></span>

### <span data-ttu-id="1fe8e-111">-內容</span><span class="sxs-lookup"><span data-stu-id="1fe8e-111">-Context</span></span>
<span data-ttu-id="1fe8e-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="1fe8e-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="1fe8e-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="1fe8e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="1fe8e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe8e-114">-DefaultProfile</span></span>
<span data-ttu-id="1fe8e-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1fe8e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fe8e-116">-GroupId</span><span class="sxs-lookup"><span data-stu-id="1fe8e-116">-GroupId</span></span>
<span data-ttu-id="1fe8e-117">指定要移除使用者的群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="1fe8e-117">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="1fe8e-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fe8e-118">-PassThru</span></span>
<span data-ttu-id="1fe8e-119">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="1fe8e-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="1fe8e-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="1fe8e-120">-UserId</span></span>
<span data-ttu-id="1fe8e-121">指定要從群組中移除的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="1fe8e-121">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="1fe8e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe8e-122">CommonParameters</span></span>
<span data-ttu-id="1fe8e-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1fe8e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe8e-124">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1fe8e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe8e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="1fe8e-125">INPUTS</span></span>

### <span data-ttu-id="1fe8e-126">ServiceManagement. PsApiManagementCoNtext （ApiManagement）</span><span class="sxs-lookup"><span data-stu-id="1fe8e-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1fe8e-127">System.object</span><span class="sxs-lookup"><span data-stu-id="1fe8e-127">System.String</span></span>

### <span data-ttu-id="1fe8e-128">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="1fe8e-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1fe8e-129">輸出</span><span class="sxs-lookup"><span data-stu-id="1fe8e-129">OUTPUTS</span></span>

### <span data-ttu-id="1fe8e-130">System.object</span><span class="sxs-lookup"><span data-stu-id="1fe8e-130">System.Boolean</span></span>

## <span data-ttu-id="1fe8e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="1fe8e-131">NOTES</span></span>

## <span data-ttu-id="1fe8e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="1fe8e-132">RELATED LINKS</span></span>

[<span data-ttu-id="1fe8e-133">附加 AzApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="1fe8e-133">Add-AzApiManagementUserToGroup</span></span>](./Add-AzApiManagementUserToGroup.md)

[<span data-ttu-id="1fe8e-134">AzApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="1fe8e-134">Get-AzApiManagementUser</span></span>](./Get-AzApiManagementUser.md)


