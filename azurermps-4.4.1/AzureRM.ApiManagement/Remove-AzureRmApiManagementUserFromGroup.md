---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F0BDB0EE-1F26-450D-9C68-34C79CE8F778
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUserFromGroup.md
ms.openlocfilehash: 2867e8eec65de040a0da61a1af960abc9797bb18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624858"
---
# <span data-ttu-id="f2c63-101">Remove-AzureRmApiManagementUserFromGroup</span><span class="sxs-lookup"><span data-stu-id="f2c63-101">Remove-AzureRmApiManagementUserFromGroup</span></span>

## <span data-ttu-id="f2c63-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f2c63-102">SYNOPSIS</span></span>
<span data-ttu-id="f2c63-103">從群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="f2c63-103">Removes a user from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2c63-104">句法</span><span class="sxs-lookup"><span data-stu-id="f2c63-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUserFromGroup -Context <PsApiManagementContext> -GroupId <String> -UserId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2c63-105">說明</span><span class="sxs-lookup"><span data-stu-id="f2c63-105">DESCRIPTION</span></span>
<span data-ttu-id="f2c63-106">**AzureRmApiManagementUserFromGroup** Cmdlet 會從現有的群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="f2c63-106">The **Remove-AzureRmApiManagementUserFromGroup** cmdlet removes a user from an existing group.</span></span>

## <span data-ttu-id="f2c63-107">示例</span><span class="sxs-lookup"><span data-stu-id="f2c63-107">EXAMPLES</span></span>

### <span data-ttu-id="f2c63-108">範例1：從群組中移除使用者</span><span class="sxs-lookup"><span data-stu-id="f2c63-108">Example 1: Remove a user from a group</span></span>
```
PS C:\>Remove-AzureRmApiManagementUserFromGroup -Context $apimContext -GroupId "0001" -UserId "0123456789"
```

<span data-ttu-id="f2c63-109">這個命令會從群組中移除使用者。</span><span class="sxs-lookup"><span data-stu-id="f2c63-109">This command removes a user from a group.</span></span>

## <span data-ttu-id="f2c63-110">參數</span><span class="sxs-lookup"><span data-stu-id="f2c63-110">PARAMETERS</span></span>

### <span data-ttu-id="f2c63-111">-內容</span><span class="sxs-lookup"><span data-stu-id="f2c63-111">-Context</span></span>
<span data-ttu-id="f2c63-112">指定 **PsApiManagementCoNtext** 物件。</span><span class="sxs-lookup"><span data-stu-id="f2c63-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f2c63-113">這個參數是必要的。</span><span class="sxs-lookup"><span data-stu-id="f2c63-113">This parameter is required.</span></span>

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

### <span data-ttu-id="f2c63-114">-GroupId</span><span class="sxs-lookup"><span data-stu-id="f2c63-114">-GroupId</span></span>
<span data-ttu-id="f2c63-115">指定要移除使用者的群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2c63-115">Specifies the ID of the group from which to remove a user.</span></span>

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

### <span data-ttu-id="f2c63-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2c63-116">-PassThru</span></span>
<span data-ttu-id="f2c63-117">指示這個 Cmdlet 會傳回 $True 的值（如果它成功的話），否則傳回 $False 的值。</span><span class="sxs-lookup"><span data-stu-id="f2c63-117">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, otherwise.</span></span>

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

### <span data-ttu-id="f2c63-118">-UserId</span><span class="sxs-lookup"><span data-stu-id="f2c63-118">-UserId</span></span>
<span data-ttu-id="f2c63-119">指定要從群組中移除的使用者識別碼。</span><span class="sxs-lookup"><span data-stu-id="f2c63-119">Specifies the ID of the user to remove from the group.</span></span>

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

### <span data-ttu-id="f2c63-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2c63-120">-DefaultProfile</span></span>
<span data-ttu-id="f2c63-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f2c63-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2c63-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2c63-122">CommonParameters</span></span>
<span data-ttu-id="f2c63-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f2c63-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2c63-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f2c63-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2c63-125">輸入</span><span class="sxs-lookup"><span data-stu-id="f2c63-125">INPUTS</span></span>

## <span data-ttu-id="f2c63-126">輸出</span><span class="sxs-lookup"><span data-stu-id="f2c63-126">OUTPUTS</span></span>

### <span data-ttu-id="f2c63-127">System.object</span><span class="sxs-lookup"><span data-stu-id="f2c63-127">System.Boolean</span></span>

## <span data-ttu-id="f2c63-128">筆記</span><span class="sxs-lookup"><span data-stu-id="f2c63-128">NOTES</span></span>

## <span data-ttu-id="f2c63-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="f2c63-129">RELATED LINKS</span></span>

[<span data-ttu-id="f2c63-130">附加 AzureRmApiManagementUserToGroup</span><span class="sxs-lookup"><span data-stu-id="f2c63-130">Add-AzureRmApiManagementUserToGroup</span></span>](./Add-AzureRmApiManagementUserToGroup.md)

[<span data-ttu-id="f2c63-131">AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="f2c63-131">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)


